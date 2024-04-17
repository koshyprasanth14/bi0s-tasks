keypad


I assigned the keypad rows, columns, and pins, along with the servo motor. Whenever a key is pressed on the keypad, that number is assigned to the variable 'key' and is displayed on the serial monitor.

 I made a variable 'count' which checks which digit of the password is being entered, and used it to write the input password into the array named 'given'. Once the array reaches the length of 8, the 'unlock' function is called, and it checks if the ciphered version of the input array matches the correct keys. 

I've included Caesar cipher as my form of encryption. 

I've tried a lot to include the LCD display but it's just not working. I only know a few causes and I've tried them one by one, but I couldn't fully figure it out.

[project link](https://wokwi.com/projects/395020501296939009)
