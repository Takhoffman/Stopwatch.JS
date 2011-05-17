**Documentation:

At the moment the stopwatch only supports doing intervals of one second.
Updating stopwatch based on milliseconds works in firefox but is running slower
in internet explorer. Strange bug that will be looked at.

Initializing a new stopwatch
var stopwatch = new Stopwatch(0);         // There are a few parameters that this will accept
var stopwatch = new Stopwatch(0, 0);      // is (days, hours)
var stopwatch = new Stopwatch(0,0,0);     // is (hours, minutes, seconds)
var stopwatch = new Stopwatch(0,0,0,0);   // is (days, hours, minutes, seconds)
var stopwatch = new Stopwatch(0,0,0,0,0); // is (days, hours, minutes, seconds, milliseconds)

The output formats for the stopwatch are as follows:
stopwatch.toString();  // output: 1.02:03:00.00 day.hour:min:sec.ms
stopwatch.toString(0); // output: 1.02:03:00 day.hour:min:sec
stopwatch.toString(1); // output: 01 day 02 hours 03 mins 00 secs
stopwatch.toString(2); // output: 1 day 2 hours 3 mins 0 secs - doesn't pad zeros
stopwatch.toString(3); // output: 26 hours 3 mins 0 secs - note - does not display days only hours
stopwatch.toString(4); // output: 26:03:00 hour:min:sec - note - does not display days only hours

Some of the other methods are:
stopwatch.toMilliseconds(); //This returns the elapsed time in milliseconds
stopwatch.toSeconds(); // This returns the elapsed time in seconds
stopwatch.toHoursRounded(); //This returns the total amount of hours rounded to two decimal places ex: 5.15
stopwatch.toJson(); //This returns a json object of the current stopwatch object comes as Days, Hours, Minutes, Seconds

**Example code:

//Create new stopwatch object and pass it the initial time
var stopwatch = new StopWatch(0) 

//Start the timer
stopwatch.start();

//Get the value of the stopwatch
stopwatch.toString(4); // Returns HH:MM:SS

//Stop the timer
stopwatch.stop();

//Reset the timer
stopwatch.reset();

**TODO:

Add some parameters for JSON object creation such as different output formats
Fix bug with internet explorer updating milliseconds method slower than firefox

Change Log:
5/17/2011 - Added the ability to initialize a stopwatch without having to create a new TimeSpan() object
5/17/2011 - Added a simple demo
5/17/2011 - got the stopwatch to update via milliseconds however am currently encountering bugs with internet explorer running slower than it should be.