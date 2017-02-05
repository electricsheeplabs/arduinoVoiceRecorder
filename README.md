# Arduino Voice Recorder
This repo contains the info you need to build your very own Arduino-based voice recorder!
Things you need:
- arduino uno, mega, or whichever (as long as it has 2kb or more of flash storage and analog inputs)
- micro sd card shield/reader for arduino 
- microphone
- mic amplifier and offset circuit (input signal conditioned for Arduino 0-5V ADC)

The code needs to be modified sightly for a given Arduino and wiring scheme. Look up how to wire your Ardunio for SPI communication, and then wire the Arduino to the microSD card reader. The code is currently set to record 10 seconds of audio to "wav0000.wav", which can be changed easily (i will add start/stop buttons and auto-naming capability soon).

MUY IMPORTANTE: Signal Conditioning
The code is set to read analog pin A5, so wire the amplified mic signal to this pin (don't forget to establish common ground with the Arduino and amp circuit!). The amplified signal is ideally centered about 2.5 V and does not drop below 0V. A sample circuit diagram is included in this repo, but it needs slight modification (such as an offset to the output) to meet the above requirements (more to come on this as well). 
 
