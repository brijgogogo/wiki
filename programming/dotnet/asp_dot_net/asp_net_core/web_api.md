= asp.net web api/ RESTful services =
- uses controllers to handle requests

[ApiController] // enables some API-specific behavirous - automatic HTTP 400 responses etc.
[Route("api/[controller]")]  // denotes base route for controller
[Produces("application/json")]
public class DemoController : ControllerBase
{

}

# ControllerBase
- BadRequest : returns 400
- NoFound : returns 404
- PhysicalFile
- TryUpdateModelAsync : invokes model binding
- TryValidateModel : invokes model validation

# attributes
- HttpPost
- ProducesResponseType
- Route
- Bind : specify prefix and properties to include for model binding
- Consumes : specifies data types that an action can accept
- Produces : specifies data types that an action returns


= sources =
https://docs.microsoft.com/en-us/aspnet/core/web-api/
