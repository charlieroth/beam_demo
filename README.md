# BeamDemo

## Intro To The BEAM

- Processes as units of work (Actor Model)
- Processes are isolated and communicate via message-passing
- Single instance can support millions of processes
- Schedulers are are mapped 1:1 with OS threads, and are responsible for scheduling processes
    - True parallel programming
- Splitting logic into processes helps both for fault and latency tolerance
- BEAM is operable, meaning you can shell into a running BEAM instance (the shell becomes one more of many processes) and perform diagnostics
- Making a system fault tolerant (a long /errant computation can’t stop other users of your system from making progress) is a lot more involved in other stacks


## Features:

### Service Dashboard

Dashboard to observe the Logging and Email services that are currently running

Logging Tab:
- Table with live updating feed of incoming logs
- Sort
- Search
- Filter

Email Tab:
- Create template
- Trigger based on log event
- Manual trigger


### Logging Service

HTTP endpoint `/log` that accepts arbitrary JSON events

JSON is processed, saved to DB, and funneled to __Service Dashboard__ for observability



### Email Service

TODO: describe service


## Resources:

[The Soul of Erlang and Elixir](https://www.youtube.com/watch?v=JvBT4XBdoUE)
