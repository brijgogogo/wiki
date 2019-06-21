= middleware =
The components that are assembled within the application request pipeline are called middleware and are responsible for handling requests and responses passing through the pipeline.

Also called request delegates.

The order in which the request delegates are defined is the order in which they will execute the request, and afterwards response in reverse.

Each middleware component in the request pipeline is responsible for invoking the next component in the pipeline or short-circuiting the pipeline.


Request delegates can be configured using Run, Map and Use extensions methods.
The first Run delegate terminates the pipeline
Chain multiple request delegates together with Use. The "next" paramter represents the next delegate in pipeline. You can short-circuit the pipeline by not calling the "next" parameter.
Map branches the request pipeline based on matches of the given request path.

# Request Delegates: Map, MapWhen, Use, Run
// Startup.Configure
public void Configure(IApplicationBuilder app)
{
    // branching based on request path
    app.Map("/skip", (skipApp) => skipApp.Run(async (context) =>
        await context.Response.WriteAsync($"Skip the line!")));

    // map based on predicate
    app.MapWhen(ctx => ctx.Request.Query.ContainsKey("branch"}, HandleBranch);

    // nesting
    app.Map("/level1", level1App => {
      level1App.Map("/level2a", level2AApp => { .. });
      level1App.Map("/level2b", level2BApp => { .. });
    });

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

= built-in middlewares =
- Authentication
- Cookie Policy
- CORS
- Excepton Handling
- Forwarded Headers
- Health Check
- Https Redirection
- response caching
- Response Compression
- compression
- routing
- sessions
- static files
- url rewrite.
- MVC
- Routing
- Web Sockets

Below middleware extensions are exposed on IApplicationBuilder through Microsoft.AspNetCore.Builder namespace.

app.UseExceptionHandler("/Error"); // development environment: app.UseDeveloperExceptionPage(), app.UseDatabaseErrorPage();
app.UseHsts();
app.UseHttpsRecirection();
app.UseStaticFiles();
app.UseCookiePolicy();
app.UseAuthentication();
app.UseSession();
app.UseResponseCompression();
app.UseMvc();


Exception handling middleware should be added first so as to catch any errors.


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


= sources =
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/middleware/index
