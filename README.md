# Indoor-air-quality-traffic-light


Indoor air quality traffic light with display and Mqtt support ( ESP32 , BME280 , CCS811 ,TM1637 , Neopixel, Mqtt)


ESP32 measures the quality of indoor air with a CCS811 and BME280 . The measurements are visualized with a neopixel strip and a 7 segment display.

The data can also be sent via Wlan and Mqtt

Attention the measurements are not calibrated and are more than tendency than absolute values!

Nevertheless it can be determined when it is useful to ventilate. Especially with regard to Covid and other cold viruses.

As housing a Led Illuminated marking field was used. This is available in many variations among others with letters.

In the code you have to declare if you want to use the Wifi.

If the wifi is active, the SSID, wifi password and the MQTT parameters must be entered. (See comments config)

#To get started:

If your ESP dosent have Micropython

Install Micropython on the ESP32

a good tutorial about it : https://docs.micropython.org/en/latest/esp32/tutorial/intro.html

I prefer Thonny https://thonny.org

In the main.py, under: ####Config###

The parameters for Wifi and Mqtt can be adjusted.

####config start#######

#config Wifi
wifi_enable = True  #True or False 
wifi_ssid = "yourSSID"
wifi_password = "yourPassword"


#config MQTT
mqtt_client = "yourClientName"
mqtt_broker = "yourBrokerIP"
mqtt_user = "yourMqttUser"
mqtt_password = "yourMqttPassword"
mqtt_port = 1883


#def MQTT  Topic
topic_co2 = b"home/livingroom/co2"
topic_tvoc = b"home/livingroom/tvoc"
topic_temp =  b"home/livingroom/temperature"
topic_humidity =  b"home/livingroom/humidity"
topic_press = b"home/livingroom/pressure"

####config end#######

Import the main.py and the libraries tm1637.py , CCS811.py ,bme280.py into the board.

Turn off the board and connect the parts to the board.

Connect CCS811, BME280 to 3.3V / GND / SCL Pin 13 /SDA Pin 5

Connect neopixel to 5V / GND / Pin 19

Connect TM1637 7Digit to 3,3V / GND / CLK Pin 17 /DIO Pin 18


Turn the Board on and enjoy :-)
