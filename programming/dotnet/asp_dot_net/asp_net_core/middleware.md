= middleware =
The components that are assembled within the application request pipeline are called middleware and are responsible for handling requests and responses passing through the pipeline.

Also called request delegates.

The order in which the request delegates are defined in the order in which they will execute the request, and afterwards response in reverse.

Built-in middlewares for: authentication, CORS, response caching, compression, routing, sessions, static files, url rewrite.

== example ==
public void Configure(IApplicationBuilder app)
{
    app.Map("/skip", (skipApp) => skipApp.Run(async (context) =>
        await context.Response.WriteAsync($"Skip the line!")));
    app.Use(async (context, next) =>
    {
        var value = context.Request.Query["value"].ToString();
        if (int.TryParse(value, out int intValue))
        {
          await context.Response.WriteAsync($"You entered a number: {intValue}");
        }
        else
        {
            context.Items["value"] = value;
            await next();
        }
    });
    app.Use(async (context, next) =>
    {
         var value = context.Items["value"].ToString();
         if (int.TryParse(value, out int intValue))
         {
            await context.Response.WriteAsync($"You entered a number: {intValue}");
         }
         else
        {
            await next();
        }
    });
    app.Use(async (context, next) =>
    {
        var value = context.Items["value"].ToString();
        context.Items["value"] = value.ToUpper();
        await next();
    });
    app.Use(async (context, next) =>
    {
        var value = context.Items["value"].ToString();
        context.Items["value"] = Regex.Replace(value, "(?<!^)[AEUI](?!$)", "*");
        await next();
    });
    app.Run(async (context) =>
    {
        var value = context.Items["value"].ToString();
        await context.Response.WriteAsync($"You entered a string: {value}");
    });
}


== example ==
You can write middleware a classes instead of inline.
The class should have:
- constructor with RequestDelegate paramter
- Invoke method which receives HttpContext

public class CustomMiddleware
{
  private readonly RequestDelegate next;

  public CustomMiddleware(RequestDelegate next) {
    this.next = next;
  }

  public async Task Invoke(HttpContext contex) {
    //logic
    next(context);
  }
}


public void Configure(IApplicationBuilder app)
{
  app.UseMiddleware<CustomMiddleware>();
}
