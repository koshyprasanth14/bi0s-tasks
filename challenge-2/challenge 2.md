challenge 2

first 'ddrxn' , 'portx' and 'pinx' are defined. ddrxn dereferences the memory location 0x24, which is the Port B Data Direction Register (given at page 72 in section 13.5.3 in the datasheet of atmega328p). similarly, portx dereferences 0x25 which is the Port B Data Register, and pinx deferences 0x23 whihc is Port B Input Pins Address. a string mc is defined which is not used in the code. 

in the setup() function, ddrxn is assigned (1<<5) which is 00100000, which is the new value for the data direction register which means the fifth pin is set as output pin. in the next line ddrxn is assigned ddrxn&~(1<<4) which passes 1 left shift 4 through a not gate and then it and ddrxn is passed through an and gate. this gives value of pin 4 as 0, which sets pin 4 as input. 

next portx is assigned |= 1 left shift 4 which gives the value of portx as 00010000. now as stated in the datasheet page 4 section 1.1.3, " As inputs, port B pins that are externally pulled low will source current if the pull-up resistors are activated." so a pull up resistor is activated in portx at pin 4. this means that if input 1 is provided in pin 4, the input recieved is 0, and vice versa. 

in the loop() function, the if condition checks if (!(pinx & (1<<4))). breaking it down, first 1 left shift 4 and pinx is passed through an and gate. say there is no input through 4, then the pull up resistor gives logic 1 at 4. now !(00010000 & 00010000) is !(1) which is 0. hence the block of else is executed, which is portx &= ~(1<<5) which essentially sets portx = 00000000. conversely, if an input 1 is provided, pin 4 of portx is set to high.

(Even though this is the logic ive undestood, the simulation shows otherwise, that is, when i provide an input into the 12th pin the led doesnt glow, and when i dont, it does. ive tried looking for anything else that changes something else in the board pins but i had no luck.)

a delay of 10 milliseconds is given.


[project link](https://wokwi.com/projects/395110017458568193)
