# IoT
# Hier beschrijf ik de stappen van LEDstrip kleur instellen via een colorpicker met Adafruit IO
  ## IOT Quickstart Adafruit IO (v.4)
  ### Introduction
    In this Notion I’ll be guiding you through the steps of making an Arduino (ESP8266) act like an expensive Philips Hue system and saving you money. We’ll be using Adafruit IO and their dashboard to change colors on      your RGB ledstrip using a color picker.
  ### Step 1: Install de Arduino IO libraries
    Het installeren van de library ging foutloos, vrij eenvoudig.
      
  ### Step 2: Adafruit IO Setup
      Aanmaken van account ook moeiteloos doorgelopen.
      
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
         Led strip reageerd niet
         Hij is goed aangesloten
       



  
