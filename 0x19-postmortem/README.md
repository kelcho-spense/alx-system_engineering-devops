# Postmortem : Error: Unable to Start Debugging on the Web Server

### Issue Summary
- On February 27th, 2023, from 15:50 to 16:10 GMT, some users were unable to
start debugging on the web server using Visual Studio.
- The impact was that users received an error message saying “Unable to start
debugging on the web server” when they tried to launch their web applications
from Visual Studio.
- The root cause was a misconfiguration of the IIS Express settings in Visual
Studio.

### Timeline
- 15:50 - The issue was detected by a user who reported it on Stack Overflow.
- 15:55 - Another user confirmed the issue and suggested checking the project
properties and the IIS configuration.
- 16:00 - A Microsoft engineer saw the post and replied with a link to a
troubleshooting guide 1.
- 16:05 - The original user followed the guide and found out that their IIS Express
settings were incorrect. They fix ed them by changing the port number and
enabling SSL.
- 16:10 - The original user confirmed that the issue was resolved and thanked the
Microsoft engineer.

### Root cause and resolution
- The issue was caused by a mismatch between the port number and SSL settings
in Visual Studio and IIS Express. This prevented Visual Studio from connecting to
the web server and launching the web application.
- The issue was fixed by editing the project properties in Visual Studio and
changing the port number and SSL settings to match those of IIS Express.

### Corrective and preventative measures
- To prevent this issue from happening again, users should always check their
project properties and make sure that they are configured to connect to the
correct web server and launch URL 1.
- To improve this issue detection and resolution, Microsoft should provide more
detailed error messages and guidance for troubleshooting common web stack
debugging issues.


