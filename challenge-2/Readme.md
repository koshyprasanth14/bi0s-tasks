Challenge 2:

First, ddrxn, portx, and pinx are defined. ddrxn dereferences the memory location 0x24, which is the Port B Data Direction Register (given on page 72 in section 13.5.3 in the datasheet of ATmega328P). Similarly, portx dereferences 0x25, which is the Port B Data Register, and pinx dereferences 0x23, which is Port B Input Pins Address. A string mc is defined which is not used in the code.

In the setup() function, ddrxn is assigned (1<<5), which is 00100000, setting the fifth pin as an output pin. In the next line, ddrxn is assigned ddrxn & ~(1<<4), which passes 1 left shift 4 through a NOT gate and then it ANDs with ddrxn. This sets pin 4 as an input.

Next, portx is assigned |= 1<<4, giving the value of portx as 00010000. As stated in the datasheet page 4, section 1.1.3, "As inputs, port B pins that are externally pulled low will source current if the pull-up resistors are activated." So, a pull-up resistor is activated in portx at pin 4. This means that if input 1 is provided on pin 4, the input received is 0, and vice versa.

In the loop() function, the if condition checks if !(pinx & (1<<4)). Breaking it down, first 1 left shift 4 and pinx are ANDed. If there is no input through pin 4, then the pull-up resistor gives logic 1 at pin 4. So, !(00010000 & 00010000) is !(1), which is 0. Hence, the block of else is executed, which is portx &= ~(1<<5), essentially setting portx = 00000000. Conversely, if an input of 1 is provided, pin 4 of portx is set to high.

Even though this is the logic I've understood, the simulation shows otherwise, that is, when I provide an input into the 12th pin, the LED doesn't glow, and when I don't, it does. I've tried looking for anything else that changes something else in the board pins, but I had no luck.

A delay of 10 milliseconds is given.

[project link](https://wokwi.com/projects/395110017458568193)
