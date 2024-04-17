16x2 lcd

Ive used the datasheet to figure out the inputs to each pins in the lcd, and arranged a circuit with 5v inpu tinto vcc and ground, and by placing a resistor in between, the voltage to the led anode and cathode. ive placed a potentiometer and connected the signal output into vd, which is used to adjust the contrast of the screen. ive placed a switch at the RS pin and enable pin. ive grounded the RW pin because i wont be using it. pins d0 across d7, ive placed a switch for each. The inputs through the pin ive given are

8 bit mode, high definition, 1 line
00110100

clear display
00000001

display on, no cursor
00001100

then, after toggling the rs switch, ive input the binary of the ascii values of each letter in 'bi0sHardware' which makes it display it. 

First i made the circuit in wokwi, but for some reason it was not working, so i tried it out in tinkercad and it worked. Hence ive attached the tinkercad link. 

[project link](https://www.tinkercad.com/things/6Kj9Q5AYUFQ-lcd-8-bit)


[screenshot](./img/screenshot.jpg)
