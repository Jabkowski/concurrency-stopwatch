# concurrency-stopwatch
A minimum working example comparing concurrency syntax in Java, Python, Go and Erlang.

## Process/Thread diagram
<img 
    style="display: block; 
           margin-left: 0;
           margin-right: auto;
           width: 90%;"
	src="graphics/thread_diagram.png"/>

## Requirements
* Maximum 3 threads or processes:  
    * counter - fast counting time base for the timer,
    * refresh - print out stopwatch format HH:MM:SS:Ms by converting counts from counter,
    * read_input - (typically main thread/process) reading user console inputs
        * \<r> reset count
        * \<q> quit,
* counter thread/process must run uninterrupted by signaling from refresh thread/process,
* only allowed to use built-in blocking time counting calls (e.g sleep),
* not allowed to make system time checking calls,
* accuracy of keeping time is of little interest (primary purpose is syntax comparison).
* minimum dependencies,
* minimum lines of code.

## Example
<img 
    style="display: block; 
           margin-left: 0;
           margin-right: auto;
           width: 70%;" 
    src="graphics/example_io.png"/>

## 
