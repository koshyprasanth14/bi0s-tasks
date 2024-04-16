traffic light

I've used an online simulator, 'PLCsimulator', to program the traffic light. In the first rung, I've put an on and off button, which also turns on the red light. In each rung, I've added a set coil for the next light and a reset coil for the previous one. After each output, I've put a timer: 5 seconds for the red light, 2 for yellow, and 4 for green. I made it such that after the loop is completed, it returns to the first rung and starts all over again, but my timers wouldn't reset. I watched as many videos as I could, read documentations, and tried out every option available in the simulator, but I couldn't reset the timer. While I was testing out everything available, I figured that if I were to turn the input off and then on again, the timers would be reset. Hence, I added a set and a reset coil for the 'off' variable. I know that that isn't the optimal method, but due to time constraints, I had to stop my research on it there.


[link](https://app.plcsimulator.online/tbqDfohBA3t9DXB9Bvo2)
