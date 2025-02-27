# ESP32-Wroom_CT_CLAMP
2 CT Clamp setup for ESP32 Wroom to monitor Washer Dryer for Home Assistant automation using ESPhome

![Photo Feb 27 2025, 05 08 08](https://github.com/user-attachments/assets/3aeb0cec-b630-49df-a5b0-3be955b8340d)


Resistors can be any value betwen 10k - 250k as long as same value is used on for both resistors. CT Clamps share the same divider and shifting circuit, as well as the stabilizing capacitor.
Be careful  which GPIO pins you use. The ones chosen here are safe, but a lot of the pins are used for other functions within the ESP32.

![circuit](https://github.com/user-attachments/assets/072a0edc-f707-4e43-ae33-e87134375335)

The idea:

30A/1V CT outputs Alternating current between -1 and +1 Volts proportional to 30 Amps. At 0 Amps it will center around 0 Volts. Since ESP32 cannot read negative voltage (its DC) we need to shift out of the negatives. For this we tap into 3v3 (3 Volt) pin, but adding it as is would shift us to -1 + 3.3 to +1 + 3.3 = 2.3V to 4.3V, that is too much as no more  than 3.3 should go into the pin on ESP32. For this we use a voltage divider, we divide 3.3v and add it to the  1v AC. This gives us range of -1 + 1.6 to +1 + 1.6 = 0.6 to 2.6 range. Perfect! To help our circuit we add a capacitor to ensure that there is non interupted and stable supply of the 1.65v from the divider.

ct_clamp platform in ESPhome handles most things for us automatically, but we need to calibrate it's readings to real readings. For this a known good source is used (I used a Killawat meter with a hot air gun). Then a table is created with known good values. It can extrapolate from those.  The more values you give the better. Its best to give it the entire range. In this case a Washer and a Dryer will almost never use more than 5A,  so I stopped my values there. The real important part is at the low end. To determine if they are running. Whethere they are pulling 2A or 10A does not matter to us. In both cases they are running.

LEDs are an optional flare, not necessary in any way.

![ESP32-wroom-pinout](https://github.com/user-attachments/assets/c9cd9af5-96f4-448b-8616-c07357d4b35c)

