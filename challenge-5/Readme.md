For Caesar cipher, we can use the equation ((p - 'A' - k + 26) % 26) + 'A', or simply make the shift and just correct an overflow if any. In my code, first I initialize a variable k which is the shift. Then I assign the string which is input through serial using 'serial.readStringUntil('\n')' into x. Array z is created to store the decoded values.

The code iterates through all elements of the input string, and first checks if it is an alphabet. If it is, it checks if it is uppercase or lowercase and shifts the character by k. It again checks if the decoded character has overflow and handles it by shifting it again by 26. If the character is not an alphabet, it skips the deciphering. In the end, the elements of the array z are printed.

[project link](https://wokwi.com/projects/394872450350902273)
