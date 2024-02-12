# Godot-Timestamp-Stopwatch
 
A thread-safe stopwatch class that uses timestamps to track time for good accuracy.

This stopwatch makes use of `Time.get_ticks_usec` to count the elapsed time.

## Usage

The stopwatch node should have a `process_mode` of `Node.PROCESS_MODE_ALWAYS` set by its script, therefore changing it in the editor will not do anything.

Exports:
* `autostart` - whether the stopwatch will start when entering the scene tree for the first time
* `stop_while_paused` - whether the stopwatch will automatically stop while the scene tree is paused, and resume after the pause ends

Methods:
* `Stopwatch.start()` - begins/resumes the stopwatch
* `Stopwatch.stop()` - stops the stopwatch
* `Stopwatch.reset()` - stops the stopwatch and sets the elapsed time to zero
* `Stopwatch.restart()` - sets the elapsed time to zero and starts the stopwatch
* `Stopwatch.is_running()` - gets whether the stopwatch is currently tracking time
* `Stopwatch.get_elapsed_microseconds() -> int` - gets the elapsed time in microseconds
* `Stopwatch.get_elapsed_milliseconds() -> int` - gets the elapsed time in milliseconds
* `Stopwatch.get_elapsed_seconds() -> float` - gets the elapsed time in seconds
