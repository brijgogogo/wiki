= asp.net core =
- cross platform
- modular, lightweight
- dependency injection within the framework
- built on top of .net core
- can be hosted on IIS, self-hosted in its own process, or even hosted inside Docker
- middleware: components that can intercept requests, and perform some logic
- configuration from files, command line, environment variables, in-memory, encrypted secret stores, ini file
- logging

== running ==
- dotnet new webapp -o <app_name>
- dotnet run
By default, ASP.NET Core binds to:
    http://localhost:5000
    https://localhost:5001 (when a local development certificate is present)


== topics ==
- [[startup]]
- [[endpoints]]
- [[host]]
- [[middleware]]
- [[routing]]
- [[filters]]
- [[hosted_services]]
- [[logging]]
- [[hosting_and_deployment]]
- [[configuration]]
- [[environments]]
- [[error_handling]]
- [[model_binding]]
- [[http_verb_attributes]]
- [[dependency_injection]]
- [[response_format]]



== flavours ==
- [[web_api]]
- [[razor_pages]]





# paths
content root: base path to any private content used by the app (default: path of executable hosting the app)
web root: base path to public, static resources, such as CSS, JavaScript, and image files (default: <content root>/wwwroot). ~/ points to web root.



# web api

= sources =
https://docs.microsoft.com/aspnet
https://docs.microsoft.com/en-us/aspnet/core/fundamentals
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/startup
https://docs.microsoft.com/en-us/aspnet/core/mvc/controllers/routing
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/middleware
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/host/web-host
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/host/web-host#content-root
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/host/generic-host
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/host/hosted-services
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/servers
https://docs.microsoft.com/en-us/aspnet/core/security/app-secrets
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration/options
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/environments
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/error-handling
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/http-requests
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/static-files


https://softwareengineering.stackexchange.com/questions/312197/benefits-of-structured-logging-vs-basic-logging
https://messagetemplates.org/
https://github.com/App-vNext/Polly
https://www.hanselman.com/blog/AddingResilienceAndTransientFaultHandlingToYourNETCoreHttpClientWithPolly.aspx

https://docs.microsoft.com/en-us/aspnet/core/web-api

