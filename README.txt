**Documentation:

At the moment the stopwatch only supports doing intervals of one second.

It's also mandatory to create a new TimeSpan() object to pass to the stopwatch, going to change this later on.

The output formats for the stopwatch are as follows:
stopwatch.toString(0); // output: 1.02:03:00 day.hour:min:sec
stopwatch.toString(1); // output: 01 day 02 hours 03 mins 00 secs
stopwatch.toString(2); // output: 1 day 2 hours 3 mins 0 secs doesn't pad zeros
stopwatch.toString(3); // output: 26 hours 3 mins 0 secs - note - does not display days only hours
stopwatch.toString(4); // output: 26:03:00 hour:min:sec - note - does not display days only hours

Some of the other methods are:
stopwatch.toMilliseconds(); //This returns the elapsed time in milliseconds
stopwatch.toHoursRounded(); //This returns the total amount of hours rounded to two decimal places e.x. 5.15

**Example code:

//Initialize the time
var initialTime = new TimeSpan(0); //Initials out to 00:00:00

//Create new stopwatch object and pass it the initial time
var stopwatch = new StopWatch(initialTime) 

//Start the timer
stopwatch.start();

//Get the value of the stopwatch
stopwatch.toString(4); // Returns HH:MM:SS

//Stop the timer
stopwatch.stop();

//Reset the timer
stopwatch.reset();

**TODO:

Create stopwatch without passing it initial TimeSpan()
Allow more options for intervals (such as milliseconds)