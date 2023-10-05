# IoT
  ## IOT Quickstart Adafruit IO (v.4)
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
      
  ### Step 2: Adafruit IO Setup
      
      
  ### Step 3: Make Adafruit IO Feed and Colorpicker
      Aanmaken van dashboard, block en colorpicker toevogen.
      
  ### Step 4: Open Arduino
       File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
       In tab ‘config.h’: plak je Adafruit IO username en Key in
         (Waar is config tab?) ---- 15 minuten zoeken en denken ----> tab? ahhhh... boven!
       In tab ‘config.h’: voer het wifi netwerk en wachtwoord in
         Hotspot aangedaan en gegevens ingevoerd in config.h
       In de Tab adafruit_14_Neopixel.ino
         #define PIXEL_PIN 5 aanpassen naar #define PIXEL_PIN D5
         Kleine aanpasing
   
  ### Step 5: Upload the code (of druk eerst op het vinkje =  Verify)
       Geverifieerd
       Verbonden
       Verander nu in Adafruit IO de kleur, dat zie je terug in de Serial monitor
         (ik begrijp dit niet. In de code of op de website)
         ik heb de kleur aangepast in de color picker, zie niks in de serial monitor
         Ik was dus niet verbonden...
         Led strip reageerd niet ----volgende dag ---> gelukt! Wie weet waarom eerst niet
         Hij is goed aangesloten
       

# Philips Hue under **€**5

By Mack Hooijman

# Introduction

In this Notion I’ll be guiding you through the steps of making an Arduino (ESP8266) act like an expensive Philips Hue system and saving you money. We’ll be using Adafruit IO and their dashboard to change colors on your RGB ledstrip using a color picker.

## What you’ll need

- Arduino Board ESP8266
- RGB LEDstrip
- microUSB to USB-C



![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/87ec4fbb-413e-4a3a-b301-2ad4c346a8fd/Untitled.png)

1. Now plug your USB into your board and pc.

**Attention!**

- The colors of the cables displayed in the image can be different for everyone.
- Double check if you plugged the cables into the right spot on the board.

# Step 2: Installing Adafruit IO libraries

We need to install a library to connect Adafruit web to the Arduino.

1. Open Arduino IDE
2. Go to the library manager and search for “Adafruit IO Arduino”
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/015b9c81-4b4a-4568-80fd-85c87cba88ee/Untitled.png)
    

[Troubleshooter]

- Doesn’t show up? Make sure you typed it correctly.

1. Click on install all
    
    

# Step 3: Create account

To use Adafruit you will have to make an account to use the dashboard.

1. Go to https://io.adafruit.com/ and make a free account.
2. Your account has a dedicated key which you need to use later in Arduino. Click on the ‘Key’ icon next to ‘New Device’. Copy your username and your key.
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/2799b5fd-318d-4f97-bd1d-ae880701c7f2/Untitled.png)
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/efa273bb-9ce4-4aac-aee0-a335deb31f87/Untitled.png)
    

# Step 4: Color picker

1. Go to the dashboard tab and create a new dashboard

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/84e58428-c4b1-4972-b099-618eb3b5cb65/Untitled.png)

1. Give it a name and navigate into your new dashboard
2. Click on the icon and select “create a new block” and select the color picker.
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/b9b14752-4a57-4422-8406-1f47614de9a8/Untitled.png)
    
3. Make a new feed called ‘color’.

# Step 5: Jump into the code

1. Go into Arduino to File > Examples > Adafruit IO Arduino > Adafruitio_14_Neopixel
2. In the 'config.h' tab: Paste your Adafruit username and your key where it says “#define IO_USERNAME” and “#define IO_KEY”

[**Important**]

The ESP8266 can only connect via the 2.4Ghz network, so be sure your wifi emits a 2.4Ghz frequency. Not sure how? Click [here](https://getnexx.com/pages/how-to-tell-if-you-have-2-4-ghz-or-5-ghz-wifi-network#:~:text=Open%20your%20networks%20panel%20from,say%202.4GHz%20or%205GHz.). 

To be 100% sure it works, you can also turn on your mobile hotspot. Be sure to emit 2.4Ghz frequency here too. Not sure how?

For Apple users: click [here](https://it-training.apple.com/tutorials/support/sup040).

For Android users: click [here](https://www.cnet.com/tech/mobile/need-to-speed-up-your-phones-wi-fi-hotspot-try-changing-this-one-android-setting/).

1. Back in in the ‘config.h’ tab, you’ll also see “#define WIFI_SSID” and “#define WIFI_PASS”. Fill in your info here.
2. In the 'adafruit_14_Neopixel.ino' tab, change: #define PIXEL_PIN 5 to #define PIXEL_PIN D5

# Step 6: Upload the code

1. Open the serial monitor and change the value to 115200 baud.
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/ee96d4b1-07df-4954-a7ab-7e8e0a1ae084/Untitled.png)
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/26628513-6d14-4ea3-93da-04c9c4769367/Untitled.png)
    
2. Press the upload icon 
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8a11f998-0b79-44b1-9e36-cfbe0f2eeb76/bd284609-0683-421d-85fd-d689d269a7e6/Untitled.png)
    
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

  
