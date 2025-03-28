# ESP32-Wroom_CT_CLAMP
2 CT Clamp setup for ESP32 Wroom to monitor Washer and Dryer for Home Assistant automation using ESPhome

## Parts List  

### Required Components  
- **2x CT Clamps** (30A/1V used (model SCT013), but 10A/1V or 20A/1V will also work)  
  - If using a CT that outputs mA, you will need to add a burden resistor to convert it to a 1V range.  
- **2x Resistors** (must be the same value, any between **10kΩ to 250kΩ** will work)  
- **1x Electrolytic (polarized) Capacitor**  
  - **10µF** works well, but anything between **1µF and 10µF** is fine.  
- **1x ESP32** with at least **2 analog pins**  
  - **ESP32-Wroom** is used here, but other ESP32 variants will also work.  

### Optional Components  
- **2x LEDs** (any color)  
  - You will need to determine the correct resistor values. Values for **blue and red LEDs** are provided by the schematic.  
- **1x Case** to house your creation.  
- **1x 5v Power Supply** to power the board (you can power it either via USB or via wiring to 5v/GND pins)
- **AHT10 board** to provide temperature and humidity for the area

![Photo Feb 27 2025, 05 08 08](https://github.com/user-attachments/assets/3aeb0cec-b630-49df-a5b0-3be955b8340d)

![image](https://github.com/user-attachments/assets/dfd6088e-8c73-4b01-954f-bd02656b928e)

![image](https://github.com/user-attachments/assets/797715c0-7382-4134-af4f-e4ab4e6dd585)

Resistors can be any value betwen 10k - 250k as long as same value is used on for both resistors. CT Clamps share the same divider and shifting circuit, as well as the stabilizing capacitor.
Be careful  which GPIO pins you use. The ones chosen here are safe, but a lot of the pins are used for other functions within the ESP32.

![image](https://github.com/user-attachments/assets/5c0a3a37-a41c-4984-9a88-4d00235be426)

The idea:

30A/1V CT outputs Alternating current between -1 and +1 Volts proportional to 30 Amps. At 0 Amps it will center around 0 Volts, at 30 Amps it will fluctuate between -1v and +1v (for different CT's this will be different treshold, i.e. 5A/1v will fluctuate at -1v to +1v at 5 Amps). Since ESP32 cannot read negative voltage (its DC) we need to shift out of the negative and make our entire sine wave be positive. For this we tap into 3v3 (3 Volt) pin, but adding it as is would shift us to -1v + 3.3v to +1v + 3.3v = 2.3V to 4.3V, that is too much as no more  than 3.3 should go into the pin on ESP32. For this we use a voltage divider, we divide 3.3v and add it to the  1v AC. This gives us range of -1v + 1.65v to +1v + 1.65v = 0.6v to 2.6v range. Perfect! Our entire fluctuating sine wave is in the positive range. To help our circuit we add a 10uF capacitor to ensure that there is non interupted and stable supply of the 1.65v from the divider.

ct_clamp platform in ESPhome handles most things for us automatically, but we need to calibrate it's readings to real readings. For this a known good source is used (I used a Killawat meter with a hot air gun). Then a table is created with known good values. It can extrapolate from those.  The more values you give the better. Its best to give it the entire range. In this case a Washer and a Dryer will almost never use more than 5A,  so I stopped my values there. The real important part is at the low end. To determine if they are running. Whethere they are pulling 2A or 10A does not matter to us. In both cases they are running.

LEDs are an optional flare, not necessary in any way.

![ESP32-wroom-pinout](https://github.com/user-attachments/assets/c9cd9af5-96f4-448b-8616-c07357d4b35c)

**Version: 03.20.2025** adds AHT10 to provide humidity and temperature for the area. This version is a separate .yaml file. Note the following differences:
  - Variant with AHT10 daughter board added (adds Humidity and temperature sensor for the area).
  - Note, overall design stays the same, however pins got moved around to reduce crosstalk (noise) created by I2C communication.
  - New Pins used for AHT10: GPIO21, GPIO22 for i2c
  - LEDs are still on GPIO17(blue) and GPIO4 (red) they were switched
  - CTClamp moved to GPIO36 and GPIO39
  - Note that there is something wrong with ESPhome code, and AHT10 boards only work if you set variant as AHT20.
