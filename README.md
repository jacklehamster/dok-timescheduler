# dok-timescheduler
Module for executing action with a delay within a game loop.

- Schedule actions within the scheduler.
- Run process with the current time. The action will get executed.

This is more or less the equivalent of setTimeout, but it is within the scheduler's process function, that can be run within a game loop;

```
const scheduler = new TimeScheduler();

schedule.scheduleAt(Date.now() + 3000, () => console.log("Action."));
// ...

//	this will display "Action." after 3 sec if schedule.process is called repeatedly. Then the action gets removed.
schedule.process(Date.now());	

```