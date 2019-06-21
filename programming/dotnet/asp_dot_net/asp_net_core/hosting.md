= hosting =

# hosting models
- in-process
app runs in the same process as its IIS worker process (w3wp.exe)
IIS handles process management
web request -> HTTP.sys driver -> IIS (port 80/443) -> IISHttpServer (in-process server implementaion for IIS) -> app middleware

UseIIS()

services.Configure<IISServerOptions>(options =>
{
  //options.AutomaticAuthentication = false; // HttpContext.User
});

- out-of-process
app runs in a process separate from IIS worker process
web request -> HTTP.sys driver -> IIS (port 80/443, w3wp.exe) -> Kestrel (random port, dotnet.exe) -> app middleware

UseIISIntegration()

services.COnfigure<IISOptions>(options =>
{
});






= sources =
https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/
