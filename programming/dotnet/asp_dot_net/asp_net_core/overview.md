= asp.net core =
- cross platform
- modular, lightweight
- dependency injection within the framework
- built on top of .net core
- can be hosted on IIS, self-hosted in its own process, or even hosted inside Docker
- middleware: components that can intercept requests, and perform some logic
- configuration from files, command line, environment variables, in-memory, encrypted secret stores, ini file
- logging

By default, ASP.NET Core binds to:
    http://localhost:5000
    https://localhost:5001 (when a local development certificate is present)

- dotnet new webapp -o aspnetcoreapp
- dotnet run

* [[startup]]
* [[endpoints]]
* [[host]]
* [[middleware]]
* [[routing]]
* [[hosted_services]]
* [[hosting_and_deployment]]

ASP.NET core includes two servers:
* [[kestrel]]
* [[HTTP.sys]]
Servers are responsible for reacting to requests made by clients by passing these requests to the application as HttpContexts.

= sources =
https://docs.microsoft.com/aspnet
