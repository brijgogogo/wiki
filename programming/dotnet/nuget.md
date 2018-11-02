= Nuget Package Manager=
Standard way for libary authors to create packages.
Provides repositories for sharing packages.
Public repository: nuget.org.
One can host their own NuGet repositories (private).
Other repositories: MyGet, Artifactory, TeamCity

In .NET Core entire BCL is distributed as a set of packages.

NuGet Tools: Visual Studio Code, Package Manager Console in VS, dotnet cli, NuGet CLI (nuget.exe)



> Install-Package NHibernate -Project Eg.Core
> Install-Package NHibernate -Version 4.1.1.4000

> dotnet add package <package-name>

:.net:
