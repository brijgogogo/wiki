= service =

A service is just a plain class that encapsulates any non user interface logic
like making http calls, logging, business rules, data access etc.

`ng generate service <serviceName>`
`ng generate service <serviceName> --module=app`


== Dependency Injection ==
You can create instance of a service are start using it in your component. But if you need the data to be shared across components, then we should register the service with Angular.

Angular creates a single instance of the service (Singleton) and shares to components via Dependency Injection.

Services are registered with Injector provided by Angular. It manages the singleton instances of services.


== example ==
demo.service.ts
import { Injectable } from '@angular/core';
@Injectable()
export class DemoSerivce {
  getItems() : IItem[] {

  }
}

== Angular Injectors ==
There is a Root Injector. When services are registered with Root Injector, they are available to any component or service in the application.

Besides, there is also an Injector for each component, mirroring the component tree. A service registered to specific component is available to that component and its child (or nested component).

* registering a service in Root Application Injector
@Injectable({
  providedIn: 'root'
})
export class DemoService {}

* registering a service in Root Application Injector (before Angular 6)
(still a valid syntax, but the "providedIn" provides better tree shaking)
@NgModule({
  providers: [DemoService]
})

* registering a service in component injector
@Component({
  providers: [DemoService]
})
export class DemoComponent {}

== Injecting the Service ==
@Component({})
export class DemoComponent {
  private _demoService;

  constructor(demoService: DemoService){
    this._demoService = demoService;
  }
}


shortcut of above code (use private/public/protected before the parameter name)

@Component({})
export class DemoComponent {
  constructor(private demoService: DemoService){}
}
