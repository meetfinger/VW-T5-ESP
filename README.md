# VW-T5-ESP
<h2> smart up the VW T5.1 MJ 2009</h2>
<h2> Disclaimer: compiled, but not testet yet</h2>

To read the current outside temperature from my car i tapped the CAN Bus. While there, i read some other stuff and added GPS. I used ESPHome because i currently use it a lot. 

Hardware-Features:
* T-Call Board with ESP32 and SIM800l Module on board
*	MCP2515 CAN Controller over SPI
*	NEO-M8N GPS Module over UART
*	MP1584EN Buck Converter 
*  2.13in Eink Display
*	DHT22, wires, ...

Software Features:
*	Read CAN Bus:
    * ID 0x623, Time
    * ID 0x571, Battery Voltage
    * ID 0x3E5, Auxilary Heater
    * ID 0x351, outside Temperature 
    * ID 0x371, Doors
* Get GPS position and send position on demand via SMS
* Read inside temperature from DHT22
* Connect to Homeassistant if car is parked near home-WiFi

Install:
1. Install Python, ESPHome, ... https://esphome.io/ 
2. Copy .yaml to computer
3. Edit as needed
3. Open terminal at .yaml position
4. Compile and upload: ```esphome run VTT2ESP.yaml```
