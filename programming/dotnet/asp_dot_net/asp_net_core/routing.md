= routing =
RouterMiddleware: map an incoming request to a route handler.

Set up in application Startup:
public void ConfigureServices(IServiceCollection services)
{
  services.AddRouting();
}

public void Configure(IApplicationBuilder app)
{
  app.UseRouter(builder=>
  {
    builder.MapRoute(string.Empty, context =>
    {
        return context.Response.WriteAsync($"Welcome to the default route!"));
    }
    builder.MapGet("foo/{name}/{surname?}", (request, response, routeData) =>
    {
      return response.WriteAsync($"Welcome to Foo, {routeData.
      Values["name"]} {routeData.Values["surname"]}"));
    }
    builder.MapPost("bar/{number:int}", (request, response, routeData) =>
    {
      return response.WriteAsync($"Welcome to Bar, number is {routeData.
      Values["number"]}"));
    }
  });
}
