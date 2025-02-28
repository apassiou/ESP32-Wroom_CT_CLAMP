# ESP32-Wroom_CT_CLAMP
2 CT Clamp setup for ESP32 Wroom to monitor Washer Dryer for Home Assistant automation using ESPhome

![Photo Feb 27 2025, 05 08 08](https://github.com/user-attachments/assets/3aeb0cec-b630-49df-a5b0-3be955b8340d)

![image](https://github.com/user-attachments/assets/dfd6088e-8c73-4b01-954f-bd02656b928e)

![image](https://github.com/user-attachments/assets/797715c0-7382-4134-af4f-e4ab4e6dd585)

Resistors can be any value betwen 10k - 250k as long as same value is used on for both resistors. CT Clamps share the same divider and shifting circuit, as well as the stabilizing capacitor.
Be careful  which GPIO pins you use. The ones chosen here are safe, but a lot of the pins are used for other functions within the ESP32.

![image](https://github.com/user-attachments/assets/001ef2bf-ee7f-42c8-aabb-9ab9c3a0f037)

The idea:

30A/1V CT outputs Alternating current between -1 and +1 Volts proportional to 30 Amps. At 0 Amps it will center around 0 Volts, at 30 Amps it will fluctuate between -1v and +1v (for different CT's this will be different treshold, i.e. 5A/1v will fluctuate at -1v to +1v at 5 Amps). Since ESP32 cannot read negative voltage (its DC) we need to shift out of the negative and make our entire sine wave be positive. For this we tap into 3v3 (3 Volt) pin, but adding it as is would shift us to -1v + 3.3v to +1v + 3.3v = 2.3V to 4.3V, that is too much as no more  than 3.3 should go into the pin on ESP32. For this we use a voltage divider, we divide 3.3v and add it to the  1v AC. This gives us range of -1v + 1.65v to +1v + 1.65v = 0.6v to 2.6v range. Perfect! Our entire fluctuating sine wave is in the positive range. To help our circuit we add a 10uF capacitor to ensure that there is non interupted and stable supply of the 1.65v from the divider.

ct_clamp platform in ESPhome handles most things for us automatically, but we need to calibrate it's readings to real readings. For this a known good source is used (I used a Killawat meter with a hot air gun). Then a table is created with known good values. It can extrapolate from those.  The more values you give the better. Its best to give it the entire range. In this case a Washer and a Dryer will almost never use more than 5A,  so I stopped my values there. The real important part is at the low end. To determine if they are running. Whethere they are pulling 2A or 10A does not matter to us. In both cases they are running.

LEDs are an optional flare, not necessary in any way.

![ESP32-wroom-pinout](https://github.com/user-attachments/assets/c9cd9af5-96f4-448b-8616-c07357d4b35c)

