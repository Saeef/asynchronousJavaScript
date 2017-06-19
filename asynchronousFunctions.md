## Asynchronous functions

asynchronous programming keeps web applications responsive by allowing multiple tasks to be processed at the same time.

<kbd>the Event Loop</kbd>
![](eventloop.png)

- The javascript runtime executes code in a single thread, meaning it can only run one statement at a time.
- Code is usually placed on the call stack before being executed
- The call stack is a segment of memory that keeps the browser queues up tasks
- The event loop, is the process in which the browser queues up tasks
- All code is run til completion by order of execution in call stack
- The event queu is initially empty, as events occur, event handlers place new tasks onto the event queue.
-     some examples ofthese events are mouse clicks, keyboard presses and timed events.

<kbd>the event queu</kbd>             
![](eventqu.png)



