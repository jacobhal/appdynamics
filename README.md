# AppDynamics

## Dashboard

The Dashboard view shows connections between services, databases etc. AppDynamics figures out what "normal" traffic should look like and when abnormalities occur, they will be flagged as either yellow or red depending on the severity.

### Database Monitoring

In the dashboard view, you can click the "Drill Down" of your database in the dashboard view and select "View in Database Monitoring".

> In the view Execution Plan -> Explain New Plan you can see the elapsed time for specific queries and see if there are any problems. For instance, someone else might be running costly queries towards your production database causing everything else to perform badly.

## Business Transaction Health

The transactions in which someone in the business refers to them as. These are automatically discovered and the only setup you might have to do yourself is to change the names to an actual meaningful name that represents the business transaction properly.

### Transaction Snapshots

A snapshot is a capture about everything about the business transactions at specific points in time. It's about the code being run, the infrastructure on which it runs upon and any other suppporting diagnostic level information.

Information that is available to us:

- Which web browser the user used.
- Potential issues, specific things like code snippets etc. that could be problematic.

> A snapshot is a _single_ transaction made by a user.

#### Drill down

Dive deeper into the parts of a specific transaction in order to see the call graph and which parts might be problematic. You can choose to go deeper into frontend, backend, external services etc.

##### Call Graph

Find the call you want to look more into and click to the right on Exit Calls / Threads.  
Next click on Drill Down Into Downstream Call in order to inspect further. In this view you can probably see what specific thing is causing your problems.

> DB & Remote Service Calls is a useful view in order to see exactly what is being executed and what operations are taking a long time.

##### Server

Inspect the server on which the application is running on.

Available information:

- Server availability
- CPU data
- Memory data
- Network issues
- Volumes (is disk space a problem? Maybe a log file is filling up the entire disk)
- Top 10 CPU/Memory consuming processes

##### Data Collectors

Diagnostic data behind the scenes, such as information about the transaction (like variables that was sent with the transaction etc.).

##### Slow Calls & Errors

Get a quick overview of slow calls.
