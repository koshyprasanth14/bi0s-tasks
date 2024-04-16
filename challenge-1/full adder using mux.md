Full adder using mux:

First, we define pins of the Arduino which will take our input logic and output it. Then, we define the pins through which we will be receiving our sum and carry of the full adder.

Since there was no 8x1 mux in Wokwi, I have made 2 8x1 mux using 2x1 mux, one which outputs the sum and the other which outputs the carry, and I connected the logic outputs from the Arduino as logic input into the mux, both for my sum mux and carry mux. According to the truth table of a full adder, I've given V inputs and grounding to pins 1, 2, 4, 7 of the sum mux and 3, 5, 6, 7 of my carry mux.

Now, as the mux receives the logic, the input into the corresponding mux pin is output, which I've set according to the truth table as mentioned above. This lets me receive the sum and carry at pins 8 and 9 of my Arduino.

I've made it print the sum and carry on the serial monitor and also digitalWrite pins 10 and 11 to show the sum and carry by lighting LEDs.
[project link](https://wokwi.com/projects/394962576967716865)
