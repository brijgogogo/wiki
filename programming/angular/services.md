= service =

A service is just a plain class that encapsulates any non user interface logic
like making http calls, logging business rules, etc.

`ng generate service <serviceName>`
`ng generate service <serviceName> --module=app`

--------------------
The @`Injectable`() decorator tells Angular that this service might itself have injected dependencies.
