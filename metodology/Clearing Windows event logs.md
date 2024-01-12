#windows 

The Windows OS stores and catalogs all actions/events performed on the system and stores them in the windows Event Log

Event logs are categorized based on the type of vents they store:
- Application logs: Stores application/program events like startup, crashes, etc.
- system logs: Stores system events like startups, reboots, etc
- Security logs: Stores security events like password changes, authentication failures,etc

Event logs can be accessed vie the Event Viewer on Windows

The event logs are the first top for any forensic investigator after a compromise has been detected it is therefore very important to clear your tracks after you are done with your assessment.

with meterpreter you can clear the logs with `clearev`