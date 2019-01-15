# openhab-MQTTv2-LED-strip

OpenHab MQTT v2 example for LED-strip using ESP8266 and Arduino 

This example uses the Holiday LED 2.0 Arduino sketch developed by TheHookup, which originally comes with support for Home Assistant, and I added support for OpenHab 2.4. 

For the original sketch and H.A. files, I refer to:
https://github.com/thehookup/Holiday_LEDs_2.0

I ported the sketch to NodeMCU (HiLetgo ESP8266 NodeMCU LUA CP2102 ESP-12E) and the Sonoff Basic. Both work just fine. For Sonoff Basic I used pin14 to program the LED strip. This requires some header soldering to enable flashing the Sonoff Basic and to get access to pin14.

I have tested it with a 1 meter 60 LED strip and a 5 meter 150 LED strip. Both the strips are WS2812b based. I used a CHINLY 5V, 10A Power Supply and a LETOUR DC 5V 30A Power Supply and either power supply works just fine with either LED strip. The 60 LED strip draws about 15 W at full white and the 150 LED strip about 35 W at full white.

Regarding OpenHab support, I am using the new MQTTv2 binding, with a things, items, sitemap and rules file. The various files are straightforward. I had to add a rules file to convert some the range for some of the slider signals as the OpenHab slider only supports 0...100 and the original sketch from the hookup uses different rnages for some fo the signals. I could have easily done these conversionin the sketch and as such not needing the rules file, but I wanted to be able to use the thehookup sketch "out of the box", such that their remains compiance with future versions.

Please give it a try and let me know your feedback or if you have any questions.

Below are two pictures of snapshots of the sitemap on my phone for this example. The first one shows the screen when scrolled up:

![Scrolled Up](scrolledUpSmall.jpg)

The second one shows the screen when scrolled down:

![Scrolled Down](scrolledDownSmall.jpg)

