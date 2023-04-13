# VW-T5-ESP
<h2> smart up the VW T5.1 MJ 2009</h2>
<h2> Disclaimer: use at your own risk</h2>

To read the current inside and outside temperature from my car i installed a ESPHome node. While there, i also included a GPS and SIM Module to act as a tracker. I used ESPHome because i currently use it a lot. 

Hardware-Features:
* T-Call Board with ESP32 and SIM800l Module on board
*	NEO-M8N GPS Module over UART
*	MP1584EN Buck Converter 
*  1.54in Eink Display
*	BME280, DHT22, wires, ...
* custom PCB to connect all modules via pin headers or plug connections
* custom enclosure to print

Software Features:
* Get GPS position and send position on demand via SMS
* Read inside temperature from DHT22 and outside temperature from BME280
* Connect to Homeassistant if car is parked near home-WiFi
* power consumption over time with 5min deepsleep and 30sec waketime 17mA

Install:
1. Install Python, ESPHome, ... https://esphome.io/ 
2. Copy .yaml to computer
3. Edit as needed
3. Open terminal at .yaml position
4. Compile and upload: ```esphome run VWT5ESP.yaml```
