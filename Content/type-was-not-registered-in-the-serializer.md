---
layout:
title: "Type Was Not Registered in the Serializer"
tags: 
origin: http://www.particular.net/Articles/type-was-not-registered-in-the-serializer
---
If you run into this exception when using NServiceBus in an ASP.NET application after upgrading the code of your app, it is usually due to files that are locked.

Exception details
-----------------


Server Error in '/' Application. Type XYZ was not registered in the serializer. Check that it appears in the list of configured assemblies/types to scan. Description: An unhandled exception occurred during the execution of the current web request. Review the stack trace for more information about the error and where it originated in the code.


Solution
--------

1.  Stop the w3svc process of the website whose code you are upgrading.
2.  Delete temporary ASP.NET files, usually found in the folder
    c:\\Windows\\Microsoft.NET\\Framework(64)\\{version}\\ .
3.  Run your application again. The exception should no longer happen.


