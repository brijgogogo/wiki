= response format =

= format-specific ActionResults =
- JsonResult

[HttpGet]
public JsonResult Get()
{
  return Json(getModels());
}

- ContentResult: plain-text

[HttpGet]
public ContentResult Get()
{
  return Content("some content");
}

[HttpGet]
public string Get() // same as ContentResult
{
  return "some content";
}


== sources ==
https://docs.microsoft.com/en-us/aspnet/core/web-api/advanced/formatting