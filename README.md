# ESP8266-MIDI
wiring of MIDI input and output

This repository is about the wiring of MIDI input and output with the ESP8266 bare chip. 

Wemos or Nodemcu users tinkers - as me - might have failed to get MIDI from other devices. This happens most likely because of the auto reset / boot circuit which is hardwired to the built-in USB UART driver of most development boards.

After doing a quite extensive research and thanks to the many open-source and forums resources I finally managed to get it working so I hope this could be useful to somebody else too!


Very important:
1. This schematics are valid for the ESP8266 bare chip only (not development boards)
2. MIDI in/out are wired respectively to RX/TX pins therefore the usb-uart serial monitor won’t work (but you can still use them to flash the chip)
3. Midi-trs is type A

BOM
  Resistors (4):
    R1:   10R
    R2:   33R
    R3:   220R
    R4:   470R
  caps (1):
    C1:   100nF
  diodes (1):
    D1:   1N4148
  Optocoupler (1):
    U1    H11L1


If you want to know more about ESP8266 bare chip wiring there’s a great guide from Pieter P:
https://tttapa.github.io/ESP8266/Chap01%20-%20ESP8266.html

The MIDI out diagram is taken from Kevin’s guide to MIDI IN for 3.3v microcontrollers (they use a raspberry Pi): https://diyelectromusic.com/2021/02/15/midi-in-for-3-3v-microcontrollers/

I preferred the “Type A” midi-trs instead of the classic DIN-5 connector. If you want to know more check this article from the MIDI association: https://midi.org/updated-how-to-make-your-own-3-5mm-mini-stereo-trs-to-midi-5-pin-din-cables

If you’re programming the ESP8266 within the Arduino environment - as I do - this wiring works with the “MIDI_DEFAULT_INSTANCE” from the Arduino Midi library by Francois Best: https://github.com/FortySevenEffects/arduino_midi_library


Let me know if I forgot to mention something .
Enjoy prototyping!

2024-12-14 CC-BY-SA 4.0 Stefano Manconi aka stziopa
