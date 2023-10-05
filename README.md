# IoT
## Philips Hue with Adafruit IO

By Nikolai Puisto

  ### Introduction
    In this Notion I’ll be guiding you through the steps of making an Arduino (ESP8266) act like an expensive Philips Hue system and saving you money. We’ll be using Adafruit IO and their dashboard to change colors on     your RGB ledstrip using a color picker.

  ## What you’ll need
    - Arduino Board ESP8266
    - RGB LEDstrip
    - microUSB to USB-C
    
  ### Step 1: Plugging everything in
    So to make this work, we obviously want to plug every cable into the right spot, so let me guide you through this process. 
      1. Grab your ESP8266 and your RGB strip
      2.  Hold your ledstrip in a way that GND is located at the top. Now grab the GND cable (cable at the top) and plug it into the GND spot on your board
      3. Grab the Din cable and plug it into D5.
      4. Grab the +5V cable and plug it into 3V3.   


1. Now plug your USB into your board and pc.

**Attention!**

- The colors of the cables displayed in the image can be different for everyone.
- Double check if you plugged the cables into the right spot on the board.

# Step 2: Installing Adafruit IO libraries

We need to install a library to connect Adafruit web to the Arduino.

1. Open Arduino IDE
2. Go to the library manager and search for “Adafruit IO Arduino”


[Troubleshooter]

- Doesn’t show up? Make sure you typed it correctly.

1. Click on install all
    
    

# Step 3: Create account

To use Adafruit you will have to make an account to use the dashboard.

1. Go to https://io.adafruit.com/ and make a free account.
2. Your account has a dedicated key which you need to use later in Arduino. Click on the ‘Key’ icon next to ‘New Device’. Copy your username and your key.


# Step 4: Color picker

1. Go to the dashboard tab and create a new dashboard


1. Give it a name and navigate into your new dashboard
2. Click on the icon and select “create a new block” and select the color picker.

    
3. Make a new feed called ‘color’.

# Step 5: Jump into the code

1. Go into Arduino to File > Examples > Adafruit IO Arduino > Adafruitio_14_Neopixel
2. In the 'config.h' tab: Paste your Adafruit username and your key where it says “#define IO_USERNAME” and “#define IO_KEY”

[**Important**]

Can't find config.h? Here it is


The ESP8266 can only connect via the 2.4Ghz network, so be sure your wifi emits a 2.4Ghz frequency. Not sure how? Click [here](https://getnexx.com/pages/how-to-tell-if-you-have-2-4-ghz-or-5-ghz-wifi-network#:~:text=Open%20your%20networks%20panel%20from,say%202.4GHz%20or%205GHz.). 

To be 100% sure it works, you can also turn on your mobile hotspot. Be sure to emit 2.4Ghz frequency here too. Not sure how?

For Apple users: click [here](https://it-training.apple.com/tutorials/support/sup040).

For Android users: click [here](https://www.cnet.com/tech/mobile/need-to-speed-up-your-phones-wi-fi-hotspot-try-changing-this-one-android-setting/).

1. Back in in the ‘config.h’ tab, you’ll also see “#define WIFI_SSID” and “#define WIFI_PASS”. Fill in your info here.
2. In the 'adafruit_14_Neopixel.ino' tab, change: #define PIXEL_PIN 5 to #define PIXEL_PIN D5

# Step 6: Upload the code

1. Open the serial monitor and change the value to 115200 baud.

    
2. Press the upload icon 

    
3. The serial monitor will now be emitting dots. It can take a moment for the board to connect to your wifi and Adafruit IO.
4. When it says ‘Adafruit IO connected’ in the serial monitor, you can head over to Adafruit IO Dashboard and click on the color picker you made earlier.
5. Choose a color
6. Your RGB ledstrip should now emit the selected color

Voila, you’re done!

[Troubleshooter]

- If you don’t see any color changes or the led is just dark, check if you’ve plugged your ledstrip in the right way.
- Still don’t see any color? Maybe you forgot to select a color in the dashboard.
- Still not helping? Check the serial monitor if your color changes are going through. Whenever you change the color, you should see "Received HEX: #19bdff” for example.
- If that’s not the case check if your username and key are correct, same goes with the wifi name and password.

  
