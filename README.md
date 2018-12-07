# Chronometer Assignment

# Introduction
This component implements a simple timer. By default it will start counting up from 0, however this can be changed. It can also count downwards by setting CountDown to (true). Also the default time display format is MM:SS, this also can be changed using setFormat.

# History
Chronometer was added in API level 1.  
[Library.png](https://github.com/n01111786/Chronometer/blob/master/image.png?raw=true) I believe the attached image shows the Library Chronometer is included in. 

# Major Method/Attributes
Here is a list of the main methods I used.

startChronometer() - This will start the timer "chronometer.start()". Furthermore, I used "chronometer.setBase(SystemClock.elapsedRealtime() - pauseOffset)" to start the timer when we click start and not when the activity starts.

pauseChronometer() - This will pause the timer "chronometer.stop()". I used "pauseOffset = SystemClock.elapsedRealtime() - chronometer.getBase()" so that when unpaused, the time would continue from where it was and not continue runnning in the background.

resetChronometer() - This will reset the timer back to 0. 

chronometer.setCountDown(true/false) - This allows you to choosed if counting up or down.

getBase() - Returns the base time.

Lastly in onCreate, I implemented "chronometer.setOnChronometerTickListener" which allows you reset the timer at a specific time and show a toast message.

# References
https://developer.android.com/reference/android/widget/Chronometer



