# ESP32-Wroom_CT_CLAMP
2 CT Clamp setup for ESP32 Wroom to monitor Washer Dryer for Home Assistant automation using ESPhome

![Photo Feb 27 2025, 05 08 08](https://github.com/user-attachments/assets/3aeb0cec-b630-49df-a5b0-3be955b8340d)


Resistors can be any value betwen 10k - 250k as long as same value is used on for both resistors. CT Clamps share the same divider and shifting circuit, as well as the stabilizing capacitor.
Be careful  which GPIO pins you use. The ones chosen here are safe, but a lot of the pins are used for other functions within the ESP32.

![circuit](https://github.com/user-attachments/assets/82207ff1-b849-4eb6-b44e-1d624d1577dc)

![Uploading circu<?xml version="1.0" encoding="utf-8"?>
<!-- Generator: Circuit Diagram, cdlibrary.dll 4.0.0.0 -->
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg version="1.1" width="880" height="580" xmlns="http://www.w3.org/2000/svg">
	<line x1="820" y1="130" x2="820" y2="135" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="820" y1="175" x2="820" y2="180" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 820,135 L 820,137 L 813,140 L 827,146 L 813,152 L 827,158 L 813,164 L 827,170 L 820,173 L 820,175" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="806" y="161" style="font-family:Arial;font-size:11px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 806, 161)">33 Ω</text>
	<text x="806" y="149" style="font-family:Arial;font-size:11px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 806, 149)">BLUE</text>
	<line x1="770" y1="150" x2="770" y2="155" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="770" y1="195" x2="770" y2="200" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 770,155 L 770,157 L 763,160 L 777,166 L 763,172 L 777,178 L 763,184 L 777,190 L 770,193 L 770,195" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="756" y="181" style="font-family:Arial;font-size:11px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 756, 181)">120 Ω</text>
	<text x="756" y="169" style="font-family:Arial;font-size:11px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 756, 169)">RED</text>
	<line x1="800" y1="350" x2="810" y2="350" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="798" y1="350" x2="798" y2="356" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="790" y1="356" x2="806" y2="356" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="793" y1="362" x2="803" y2="362" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="796" y1="368" x2="800" y2="368" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="30" y1="540" x2="40" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="28" y1="540" x2="28" y2="546" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="20" y1="546" x2="36" y2="546" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="23" y1="552" x2="33" y2="552" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="26" y1="558" x2="30" y2="558" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="810" y1="320" x2="810" y2="350" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="770" y1="320" x2="820" y2="320" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="820" y1="270" x2="820" y2="320" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="770" y1="270" x2="770" y2="320" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="820" y1="180" x2="820" y2="240" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="650" y1="130" x2="820" y2="130" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="770" y1="200" x2="770" y2="250" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="660" y1="150" x2="770" y2="150" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="770" y1="240" x2="770" y2="270" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 770,262 M 762,262 L 778,262 M 770,262 L 778,247 L 762,247 L 770,262" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 770,260 M 781,258 L 789,266 M 790,267 L 788,263 L 786,265 L 790,267 L 788,263" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 770,260 M 774,264 L 782,272 M 783,273 L 781,269 L 779,271 L 783,273 L 781,269" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="820" y1="240" x2="820" y2="270" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 820,262 M 812,262 L 828,262 M 820,262 L 828,247 L 812,247 L 820,262" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 820,260 M 831,258 L 839,266 M 840,267 L 838,263 L 836,265 L 840,267 L 838,263" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 820,260 M 824,264 L 832,272 M 833,273 L 831,269 L 829,271 L 833,273 L 831,269" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="250" y1="420" x2="280" y2="420" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="250" y1="270" x2="250" y2="420" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="250" y1="60" x2="250" y2="220" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="250" y1="220" x2="250" y2="221" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="250" y1="269" x2="250" y2="270" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 250,221 A 1.5,2 90 1 1 250,233 M 250,233 A 1.5,2 90 1 1 250,245 M 250,245 A 1.5,2 90 1 1 250,257 M 250,257 A 1.5,2 90 1 1 250,269" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="242" y="245" style="font-family:Arial;font-size:11px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 242, 245)">30A/1V</text>
	<line x1="250" y1="60" x2="540" y2="60" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="280" y1="480" x2="420" y2="480" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="40" y1="460" x2="40" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="40" y1="450" x2="40" y2="460" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="40" y1="450" x2="160" y2="450" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="40" y1="540" x2="160" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="210" y1="540" x2="280" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="280" y1="450" x2="280" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="160" y1="540" x2="181" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="189" y1="540" x2="210" y2="540" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="181" y1="526" x2="181" y2="554" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 189,540 M 191,553.5 A 15,25 0 0 1 191,526.5" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="185" y="520" style="font-family:Arial;font-size:11px;text-anchor:middle" dominant-baseline="baseline" transform="rotate(0, 185, 520)">10 µF</text>
	<line x1="470" y1="300" x2="470" y2="480" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="470" y1="300" x2="660" y2="300" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="660" y1="220" x2="660" y2="300" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="430" y1="80" x2="540" y2="80" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="430" y1="80" x2="430" y2="220" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<rect x="550" y="40" width="100" height="190" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-width:2" />
	<text x="600" y="30" style="font-family:Arial;font-size:11px;text-anchor:middle" dominant-baseline="middle" transform="rotate(0, 600, 30)">ESP32-Wroom</text>
	<line x1="540" y1="50" x2="550" y2="50" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="50" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 50)">EN</text>
	<text x="546" y="48" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 48)"></text>
	<line x1="650" y1="50" x2="660" y2="50" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="50" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 50)">GPIO23</text>
	<text x="654" y="48" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 48)">VSPI MOSI</text>
	<line x1="540" y1="60" x2="550" y2="60" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="60" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 60)">GPIO36</text>
	<text x="546" y="58" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 58)">ADC1 CH0</text>
	<line x1="650" y1="60" x2="660" y2="60" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="60" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 60)">GPIO22</text>
	<text x="654" y="58" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 58)">I2C SCL</text>
	<line x1="540" y1="70" x2="550" y2="70" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="70" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 70)">GPIO39</text>
	<text x="546" y="68" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 68)">ADC1 CH3</text>
	<line x1="650" y1="70" x2="660" y2="70" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="70" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 70)">GPIO1</text>
	<text x="654" y="68" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 68)">UART 0 TX</text>
	<line x1="540" y1="80" x2="550" y2="80" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="80" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 80)">GPIO34</text>
	<text x="546" y="78" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 78)">ADC1 CH6</text>
	<line x1="650" y1="80" x2="660" y2="80" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="80" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 80)">GPIO3</text>
	<text x="654" y="78" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 78)">UART 0 RX</text>
	<line x1="540" y1="90" x2="550" y2="90" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="90" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 90)">GPIO35</text>
	<text x="546" y="88" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 88)">ADC1 CH7</text>
	<line x1="650" y1="90" x2="660" y2="90" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="90" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 90)">GPIO21</text>
	<text x="654" y="88" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 88)">I2C SDA</text>
	<line x1="540" y1="100" x2="550" y2="100" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="100" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 100)">GPIO32</text>
	<text x="546" y="98" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 98)">ADC1 CH4</text>
	<line x1="650" y1="100" x2="660" y2="100" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="100" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 100)">GPIO19</text>
	<text x="654" y="98" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 98)">VSPI MISO</text>
	<line x1="540" y1="110" x2="550" y2="110" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="110" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 110)">GPIO33</text>
	<text x="546" y="108" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 108)">ADC1 CH5</text>
	<line x1="650" y1="110" x2="660" y2="110" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="110" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 110)">GPIO18</text>
	<text x="654" y="108" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 108)">VSPI CLK</text>
	<line x1="540" y1="120" x2="550" y2="120" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="120" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 120)">GPIO25</text>
	<text x="546" y="118" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 118)">ADC2 CH8</text>
	<line x1="650" y1="120" x2="660" y2="120" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="120" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 120)">GPIO5</text>
	<text x="654" y="118" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 118)">VSPI CS0</text>
	<line x1="540" y1="130" x2="550" y2="130" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="130" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 130)">GPIO26</text>
	<text x="546" y="128" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 128)">ADC2 CH9</text>
	<line x1="650" y1="130" x2="660" y2="130" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="130" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 130)">GPIO17</text>
	<text x="654" y="128" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 128)">UART 2 TX</text>
	<line x1="540" y1="140" x2="550" y2="140" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="140" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 140)">GPIO27</text>
	<text x="546" y="138" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 138)">ADC2 CH7</text>
	<line x1="650" y1="140" x2="660" y2="140" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="140" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 140)">GPIO16</text>
	<text x="654" y="138" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 138)">UART 2 RX</text>
	<line x1="540" y1="150" x2="550" y2="150" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="150" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 150)">GPIO14</text>
	<text x="546" y="148" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 148)">ADC2 CH6</text>
	<line x1="650" y1="150" x2="660" y2="150" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="150" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 150)">GPIO4</text>
	<text x="654" y="148" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 148)">ADC2 CH0</text>
	<line x1="540" y1="160" x2="550" y2="160" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="160" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 160)">GPIO12</text>
	<text x="546" y="158" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 158)">ADC2 CH5</text>
	<line x1="650" y1="160" x2="660" y2="160" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="160" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 160)">GPIO2</text>
	<text x="654" y="158" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 158)">ADC2 CH2</text>
	<line x1="540" y1="170" x2="550" y2="170" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="170" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 170)">GPIO13</text>
	<text x="546" y="168" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 168)">ADC2 CH4</text>
	<line x1="650" y1="170" x2="660" y2="170" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="170" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 170)">GPIO15</text>
	<text x="654" y="168" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 168)">ADC2 CH3</text>
	<line x1="540" y1="180" x2="550" y2="180" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="180" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 180)">GPIO9</text>
	<text x="546" y="178" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 178)">SHD/SD2</text>
	<line x1="650" y1="180" x2="660" y2="180" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="180" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 180)">GPIO0</text>
	<text x="654" y="178" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 178)">ADC2 CH1</text>
	<line x1="540" y1="190" x2="550" y2="190" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="190" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 190)">GPIO10</text>
	<text x="546" y="188" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 188)">SWP/SD3</text>
	<line x1="650" y1="190" x2="660" y2="190" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="190" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 190)">GPIO8</text>
	<text x="654" y="188" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 188)">SDI/SD1</text>
	<line x1="540" y1="200" x2="550" y2="200" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="200" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 200)">GPIO11</text>
	<text x="546" y="198" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 198)">CSC/CMD</text>
	<line x1="650" y1="200" x2="660" y2="200" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="200" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 200)">GPIO7</text>
	<text x="654" y="198" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 198)">SDO/SD0</text>
	<line x1="540" y1="210" x2="550" y2="210" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="210" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 210)">GND</text>
	<text x="546" y="208" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 208)"></text>
	<line x1="650" y1="210" x2="660" y2="210" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="210" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 210)">GPIO6</text>
	<text x="654" y="208" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 208)">SCK/CLK</text>
	<line x1="540" y1="220" x2="550" y2="220" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="554" y="220" style="font-family:Arial;font-size:10px;text-anchor:start" dominant-baseline="middle" transform="rotate(0, 554, 220)">VIN</text>
	<text x="546" y="218" style="font-family:Arial;font-size:8px;text-anchor:end" dominant-baseline="baseline" transform="rotate(0, 546, 218)"></text>
	<line x1="650" y1="220" x2="660" y2="220" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="646" y="220" style="font-family:Arial;font-size:10px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 646, 220)">3V3</text>
	<text x="654" y="218" style="font-family:Arial;font-size:8px;text-anchor:start" dominant-baseline="baseline" transform="rotate(0, 654, 218)"></text>
	<line x1="280" y1="420" x2="280" y2="450" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="210" y1="450" x2="280" y2="450" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="280" y1="420" x2="430" y2="420" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="430" y1="270" x2="430" y2="420" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="430" y1="220" x2="430" y2="221" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="430" y1="269" x2="430" y2="270" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 430,221 A 1.5,2 90 1 1 430,233 M 430,233 A 1.5,2 90 1 1 430,245 M 430,245 A 1.5,2 90 1 1 430,257 M 430,257 A 1.5,2 90 1 1 430,269" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="422" y="245" style="font-family:Arial;font-size:11px;text-anchor:end" dominant-baseline="middle" transform="rotate(0, 422, 245)">30A/1V</text>
	<line x1="160" y1="450" x2="165" y2="450" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="205" y1="450" x2="210" y2="450" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 165,450 L 167,450 L 170,443 L 176,457 L 182,443 L 188,457 L 194,443 L 200,457 L 203,450 L 205,450" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="185" y="436" style="font-family:Arial;font-size:11px;text-anchor:middle" dominant-baseline="baseline" transform="rotate(0, 185, 436)">10 kΩ</text>
	<line x1="420" y1="480" x2="425" y2="480" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<line x1="465" y1="480" x2="470" y2="480" style="stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<path d="M 425,480 L 427,480 L 430,473 L 436,487 L 442,473 L 448,487 L 454,473 L 460,487 L 463,480 L 465,480" style="fill-opacity:0;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-linecap:square;stroke-width:2" />
	<text x="445" y="466" style="font-family:Arial;font-size:11px;text-anchor:middle" dominant-baseline="baseline" transform="rotate(0, 445, 466)">10 kΩ</text>
	<ellipse cx="40" cy="540" rx="2" ry="2" style="fill-opacity:1;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-width:2" />
	<ellipse cx="810" cy="320" rx="2" ry="2" style="fill-opacity:1;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-width:2" />
	<ellipse cx="280" cy="420" rx="2" ry="2" style="fill-opacity:1;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-width:2" />
	<ellipse cx="280" cy="480" rx="2" ry="2" style="fill-opacity:1;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-width:2" />
	<ellipse cx="280" cy="450" rx="2" ry="2" style="fill-opacity:1;fill:rgb(0, 0, 0);stroke:rgb(0, 0, 0);stroke-width:2" />
</svg>it.svg…]()


The idea:

30A/1V CT outputs Alternating current between -1 and +1 Volts proportional to 30 Amps. At 0 Amps it will center around 0 Volts. Since ESP32 cannot read negative voltage (its DC) we need to shift out of the negatives. For this we tap into 3v3 (3 Volt) pin, but adding it as is would shift us to -1 + 3.3 to +1 + 3.3 = 2.3V to 4.3V, that is too much as no more  than 3.3 should go into the pin on ESP32. For this we use a voltage divider, we divide 3.3v and add it to the  1v AC. This gives us range of -1 + 1.6 to +1 + 1.6 = 0.6 to 2.6 range. Perfect! To help our circuit we add a capacitor to ensure that there is non interupted and stable supply of the 1.65v from the divider.

ct_clamp platform in ESPhome handles most things for us automatically, but we need to calibrate it's readings to real readings. For this a known good source is used (I used a Killawat meter with a hot air gun). Then a table is created with known good values. It can extrapolate from those.  The more values you give the better. Its best to give it the entire range. In this case a Washer and a Dryer will almost never use more than 5A,  so I stopped my values there. The real important part is at the low end. To determine if they are running. Whethere they are pulling 2A or 10A does not matter to us. In both cases they are running.

LEDs are an optional flare, not necessary in any way.

![ESP32-wroom-pinout](https://github.com/user-attachments/assets/c9cd9af5-96f4-448b-8616-c07357d4b35c)

