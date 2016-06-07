# SRP - Single Responsibility Principles
A class should one, and only one, reason to change


An object should only have one reason to change


The example does not have a single responsibility.
Solve by extracting some of the actions into their own classes.


1) Why should SalesReporter have any interest in the authenticated user?
- It's application logic, doesn't belong in SalesReporter.  It stops us using SalesReporter if we don't have an authenticated
user (e.g. if it is part of a service, or accessed via API).  Shouldn't be responsibility of SalesReporter

2) What if we wanted to chang our DB persistence layer or change the formatting of the output?
- This class shouldn't be responsible for understanding our persistence layer.  Perhaps should be injected through a constructor?

