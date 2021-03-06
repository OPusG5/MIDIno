# MIDIno
MIDI (through standard 5-PIN DIN MIDI cables) to BLE-MIDI bridging with Arduino-compatible boards project.    

This project was inspired by **[Matt Sieren (sieren) blidino Arduino USB-MIDI to BLE-MIDI project] (https://github.com/sieren/blidino)**. 
I would like to thank him because his work made this possible as all the BLE-MIDI to MIDI parsing part is taken from his blidino project ( see [BLEParser.h](https://github.com/sieren/blidino/blob/master/nRF51822-BLEMIDI/BLEParser.h) ).

The purpose of this project is to allow MIDI devices that doesn't support USB-MIDI (vintage synths for example) to communicate wires-free through the Midi Manufacturers Association MIDI over Bluetooth Low Energy (BLE-MIDI) protocol.   

# Supported Boards

[RedBearLab nRF51822](https://github.com/popcornell/MIDIno/tree/master/MIDI_to_BLE-MIDI_bridge%20nRF51822)

Currently the only board supported is the **redbearlab nRF51822** Arduino-compatible Board. 

This repo contains the code for the Arduino IDE but as this same board supports [mbed OS](https://www.mbed.com/en/development/mbed-os/) ( see [redbearslab nRF51822 description](http://redbearlab.com/redbearlab-nrf51822/) ) the program was originally developed using that platform ([mbed Compiler](https://developer.mbed.org/handbook/mbed-Compiler)) .    

Also currently this Arduino IDE port here _lacks of uart software buffering_ it should be ported in the future from the original program. 





###As such i recommend, for now , to use instead the mbed OS version available here [MIDI-to-BLE-MIDI-bridge (mbed OS)](https://developer.mbed.org/users/popcornell/code/MIDI-to-BLE-MIDI-bridge/).






#BLE-MIDI 

The Midi Manufacturers Association MIDI over Bluetooth Low Energy (BLE-MIDI) Specification is available, upon free registration, here at Midi Manufacturers Association official site: https://www.midi.org/specifications/item/the-midi-1-0-specification. 

Alternatively as the Midi Manufacturers Association de-facto adopted Apple BLE-MIDI Specification one can consult: 
[Apple Bluetooth Low
Energy MIDI
Specification](https://developer.apple.com/bluetooth/Apple-Bluetooth-Low-Energy-MIDI-Specification.pdf)


#Videos 

<a href="http://www.youtube.com/watch?feature=player_embedded&v=TbiXCS43HPc
" target="_blank"><img src="http://img.youtube.com/vi/TbiXCS43HPc/0.jpg" 
alt="Video" width="260" height="180" border="10" /></a>


# Alternative Purpose: Enabling BLE-MIDI on Windows 

This program can also be used to enable a **Windows/Linux machine to communicate with BLE-MIDI hardware**.
There is no need for additional hardware only the board and a micro USB cable. 
The PC must run a Serial to MIDI software such as **Hairless MIDI Serial**.
Also a software which enables multiple virtual MIDI ports is required on Windows such as **loopMIDI**. 

Note: as MIDI standard 31250 baud rate is not supported by USB ports ( but there are workarounds especially in Linux ) change **BAUD_RATE** in **config.h** to a more common value for USB.


<a href="http://www.youtube.com/watch?feature=player_embedded&v=hbhb36hEA3s
" target="_blank"><img src="http://img.youtube.com/vi/hbhb36hEA3s/0.jpg" 
alt="Video" width="260" height="180" border="10" /></a>

