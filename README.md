# IoT
Hier beschrijf ik de stappen van LEDstrip kleur instellen via een colorpicker met Adafruit IO
  IOT Quickstart Adafruit IO (v.4)
    Stap 1: Installeer de Arduino IO libraries
      Het installeren van de library ging foutloos, vrij eenvoudig.
    Stap 2: Adafruit IO Setup
      Aanmaken van account ook moeiteloos doorgelopen.
    Stap 3: Adafruit IO Feed en Colorpicker aanmaken
      Aanmaken van dashboard, block en colorpicker toevogen.
    Stap 4: Arduino gebruiken
       File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
       In tab ‘config.h’: plak je Adafruit IO username en Key in
         (Waar is config tab?) ---- 15 minuten zoeken en denken ----> tab? ahhhh... boven!
       In tab ‘config.h’: voer het wifi netwerk en wachtwoord in
         Hotspot aangedaan en gegevens ingevoerd in config.h
       In de Tab adafruit_14_Neopixel.ino
         #define PIXEL_PIN 5 aanpassen naar #define PIXEL_PIN D5
         Kleine aanpasing
    Stap 5: Code uploaden (of druk eerst op het vinkje =  Verify)
       Geverifieerd
       Verander nu in Adafruit IO de kleur, dat zie je terug in de Serial monitor
         (ik begrijp dit niet. In de code of op de website)
         ik heb de kleur aangepast in de color picker, zie niks in de serial monitor
         
       



  
