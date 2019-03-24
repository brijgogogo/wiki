= kestrel =
Kestrel is a cross-platform web server for ASP.NET Core.
Based on libuv

You can use Kestrel by itself or with a reverse proxy server, such as Internet Information Services (IIS), Nginx, or Apache.

ASP.NET Core IIS Module (ANCM), an IIS module, must be installed in IIS for the IIS integration to work.

When Kestrel is configured to listen on a port, Kestrel handles all of the traffic for that port regardless of requests' Host headers. A reverse proxy that can share ports has the ability to forward requests to Kestrel on a unique IP and port.

* [[reverse-proxy]]

= usage =
The Microsoft.AspNetCore.Server.Kestrel package is included in the Microsoft.AspNetCore.App metapackage (ASP.NET Core 2.1 or later).

var host = new WebHostBuilder()
        .UseContentRoot(Directory.GetCurrentDirectory())
        .UseKestrel()
        .UseIISIntegration()
        .UseStartup<Startup>()
        .ConfigureKestrel((context, options) =>
        {
            // Set properties and call methods on options
            options.Limits.MaxConcurrentConnections = 100;
            options.Limits.MaxConcurrentUpgradedConnections = 100;
            options.Limits.MaxRequestBodySize = 10 * 1024;
            options.Limits.MinRequestBodyDataRate = new MinDataRate(bytesPerSecond: 100, gracePeriod: TimeSpan.FromSeconds(10));
            options.Limits.MinResponseDataRate = new MinDataRate(bytesPerSecond: 100, gracePeriod: TimeSpan.FromSeconds(10));
            options.Listen(IPAddress.Loopback, 5000);
            options.Listen(IPAddress.Loopback, 5001, listenOptions =>
            {
              listenOptions.UseHttps("testCert.pfx", "testPassword");
            });
        })
        .Build();

    host.Run();

= sources =
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/servers/kestrel?view=aspnetcore-2.2
