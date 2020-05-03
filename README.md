# Indoor-air-quality-traffic-light
Indoor air quality traffic light with display and Mqtt support ( ESP32 , BME280 , CCS811 , Neopixel, Mqtt)  

ESP32 measures the quality of indoor air with a CCS811 and BME280 . The measurements are visualized with a neopixel strip and a 7 segment display.

The data can also be sent via Wlan and Mqtt 

Attention the measurements are not calibrated and are more than tendency than absolute values!

Nevertheless it can be determined when it is useful to ventilate. Especially with regard to Covid and other cold viruses. 

As housing a Led Illuminated marking field was used. This is available in many variations among others with letters.

In the code you have to declare if you want to use the Wifi.

If the wifi is active, the SSID, wifi password and the MQTT parameters must be entered. (See comments config)

To get started:
  Install micropython on your ESP32
  Connect CCS811, BME280 to 3,3V/GND/SCL/SDA
  Connect Neopixel to 5V/GND/Pin
  Connect 7Digit to 3,3V/GND/Clk/Dio



