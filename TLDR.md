This is a TLDR that I wish I had available when I first stated learning about observability.

This TLDR assumes you have written some code and maybe even made your own application.

### Observability 
The mathematical definition of Observability:
> a measure of how well internal states of a system can be inferred from knowledge of its external outputs
Applied to software development, how well can you tell what your application / server / system is doing from its output without adding more code to tell you what it's doing?

It might be helpful to note that the definition of Observability might vary depending on who you're talking to, but for now, we're going to stick to the above.

### Telemetry
Data outputted from a system about itself.  Typically, when people say telemetry, they are referring to logs, metrics, traces, or all of them.  But yes, even your garden variety print statements can be considered telemetry if its telling you more about its internal workings!

### Instrument / Instrumenting
To instrument is to add code with the purpose of emitting telemetry.

### Backend
The final destination to which you want to send your telemetry.

### Logs
Like a print statement, but production scale.  Logs are usually collected to a central location, readable in real time, and queryable.

> I define a log as a programmatic output that a dev thought would be useful but is missing key details
~ Preocts

> like nice mail you send to yourself in the future
~ Alvidoodle

> "A logbook (a ship's logs or simply log) is a record of important events in the management, operation, and navigation of a ship."
~ foobaer, citing wikipedia

### Metrics
Outputs that can be graphed into squiggly lines, shark fins, sawtooths.

### Traces
A trace is composed of one or more spans (you can think of a span as a log for now) that, collectively, tell the story of all that happened to complete one unit of work.

### Span
A span is like a structured log and it knows which log happened before itself, and which larger "story" of logs it is a part of (trace_id)