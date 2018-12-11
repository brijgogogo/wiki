VS Code:
Ctrl + tilde : terminal
(use Git Bash as terminal in VS Code)
Alt + Shift + F : format

Extensions:
Angular v5 Snippets (John Papa)
Bracket Pair Colorizer
Emmet (already part of VS)

Browser extension:
Augury

lorempixel.com

angular-cli
npm install -g @angular/cli
ng help
ng new <project_name>
ng serve --open: builds and serves app in browser
ng build
ng generate component <comp_name>
ng g c components/users --spec=false



== Components ==
Component: Pieces of UI
Class, Template
Bind from/to class <-> tempalte
Root App Component

import { Component} from '@angular/core';

@Component({
	selector: 'my-app',
	//template: '<h1>Hello {{name}}</h1>',
	templateUrl: './app.component.html',
	styleUrls: ['./app.component.css'],
	//styles: [`
	//	h2 { color: blue }
	//`]
})
export class AppComponent
{
	name = 'Angular';
	
	constructor() {
		this.sayHello();
	}
	
	sayHello() {
		console.log(`Hello ${this.name}`);
	}
}


<body>
	<my-app>Loading AppComponent content here ...</my-app>
</body>

> ng g component components/my-component

import { OnInit} from '@angular/core';
export class UserComponent implements OnInit {
	ngOnInit() {
	// set property values here
	}
}


== Template Syntax ==
<ul>
	<li *ngFor="let user of users">
		{{ user.firstName }}
	</li>
</ul>

<ul *ngIf="showExtended">
...
</ul>

<ul *ngIf="users?.length > 0">
...
</ul>

<ul *ngIf="users.length > 0; else noUsers">
</ul>
<ng-template #noUsers>No Users found</ng-template>


== property binding ==
<button [disabled]="!enabledAdd" class="btn">Add</button>
<img [src]="user.image" alt="" >
<img src="{{user.image}}" >
<img bind-src="user.image" >
<span [textContent]="user.firstName"></span>

== class binding ==
<li class="card card-body" [class.bg-light]="user.isActive"></li>

<button [ngClass]="currentClasses">Add<button>

currentClasses = {};
this.currentClasses = {
	'btn-success': this.enableAdd,
	'big-text': this.showExtended
}


== style binding ==
<li [style.border-color]="user.isActive ? 'green' : ''"></li>
<h3 [ngStyle]="currentStyles"></h3>

currentStyles= {};
this.currentStyles = {
	'padding-top' = this.showExtended ? '0' : '40px',
	'font-size': this.showExtended  ? '' : '40px'
}

== pipes ==
{{ user.firstName | uppercase }}
{{ user.firstName | lowercase }}
{{ user.balance | currency }}
{{ user.balance | currency:"GBP" }}
{{ user.balance | currency:"GBP":"code" }}
{{ user.balance | currency:"GBP":"symbol" }}
{{ user.dob | date }}
{{ user.dob | date:"mm/dd/yyyy" }}
{{ user.dob | date:"shortDate" }}
{{ user.dob | date:"fullDate" }}
{{ user.dob | date:"shortTime" }}
{{ user.dob | date:"longTime" }}
{{ 5 | number:"1.2" }}
{{ 1 | percent }}
{{ 0.5 | percent }}

<li ngNonBindable>{{ 5 | number:"2.4" }}</li>


== events, forms ==
<button (click)="fireEvent($event)" (mouseOver)="fireEvent($event)">Add</button>

fireEvent(e) {
	console.log(e.type)
}

<button (click)="addUser({firstName: 'Brij', lastName: 'Sharma'})">Add</button>

<small><button (click)="toggleHide(user)" class="btn btn-dark btn-sm">Toggle</button></small>
toggleHide(user: User) {
	user.hide = !this.hide;
}

<small><button (click)="user.hide = !user.hide" class="btn btn-dark btn-sm">Toggle</button></small>

== keyboard and input events ==
<form (submit)=onSubmit($event)>
</form>
onSubmit(e) {
	e.preventDefault();
}

<input (keydown)="fireEvent($event) type="text" name="firstName">
fireEvent(e) {
	console.log(e.target.value);
}

== ngmodel & 2 way data binding ==
import { FormsModule } from '@angular/Forms'
//add to @NgModule

<input type="text" [(ngModel)]="user.firstName" name="firstName" >
<button (click)="addUser()" [disabled]="user.firstname == '' || user.lastName == ''">Add user</button>














= .net core testing =
dotnet new xunit
dotnet add reference project_to_test.csproj
dotnet test

Microsoft.AspNetCore.TestHost
Unit, Integration tests

= .net core logging =
Microsoft.Extensions.Logging package
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging/?view=aspnetcore-2.1&tabs=aspnetcore2x

= .net core configuration =
Microsoft.Extensions.Configuration package
https://www.paraesthesia.com/archive/2018/06/20/microsoft-extensions-configuration-deep-dive/

key/value pairs
keys: case-insensitive
values: strings
hierarchy delimiter: :
flatten structure
configuration provider: json/xml/ini/environment variables/command line parameters

follow a precedence like: appsettings.json -> appsettings.{EnvironmentName}.json -> environment variables -> command line parameters

var builder = new ConfigurationBuilder();
builder.AddJsonFile("appsettings.json");
var root = builder.Build();
var value = root["logging:enabled"]; // returns string

Microsoft.Extensions.Configuration.Binder package
root.GetValue<bool>("logging:enabled");
root.GetSection("logging").Get<LoggingSection>();// LoggingSection is your custom class which maps to properties of sub-section in settings file
use DataAnnotations to validate


= Software Architect =
makes high-level design choices
dictates technical standards (coding standards, tools, platforms)

arechitecture level:
application : focus on one single application. detailed, low level design. Communication: single team
solution : fulfill a business need (high, low-level design). Communication: multiple teams
enterprise : focus on multiple solutions. High level, abstract design. Communication: across organization

skills: design, decide, simplify, code, document, communicate, estimate, balance, consult, market








= Javascript =
sinonjs : stubs, mocks
proxyquire: 
avajs : test runner


= monitoring microservices applications =
ELS-Stack
Prometheus

micrrservices technologies: MS Azure Contianer Service, Azure Service Fabric, CoreOS, Docker, Swarm, Kubernetes, Mesosphere, OpenShift, Apprenda






= Docker =
Container - [App, Libs, Dependencies]
Docker hub/store

docker run nodejs
docker run redis
docker run mongodb

Image: template used to create container
An instance of an image is called a container.

= choosing a tech stack = 
Understanding the project
Scope, Budget, Timeframe
One-timer or long-term project
Can technical debt be handled (if hasted)
How secure ?
Can I handle the project ?
tech stack: Is it overkill, or under-powered ?
tech stack : well documented, supported
tech stack: risks ?
tech stack: developer availability at what cost ?


= GraphQL =
GraphQL is a query language for APIs
It is a specificatin of a query language
implementations: Apollo Client, Relay
strongly-typed query language
allows to cherry-pick the data needed without receiving any extraneous data from the backend

everything goes through a single endpoint, typically named graphql by convention


= F# =
https://fsharpforfunandprofit.com/posts/fsharp-in-60-seconds/
https://fsharpforfunandprofit.com/posts/key-concepts/
https://fsharpforfunandprofit.com/posts/discriminated-unions/
https://fsharpforfunandprofit.com/posts/records/

type inference
F# types: tuple, record, union
list, seq
List.fold, List.map, List.iter, List.sum, List.zip
Seq.filter, Seq.groupBy
String.length
pipe |>
composition >>
composition: build larger systems from smaller ones
statement oriented vs expression oriented

* product types
type IntAndBool = {intPart: int; boolPart: bool}
let x = {intPart=1; boolPart=false}

* sum types:
type IntOrBool =
	| IntChoice of int
	| BoolChoice true
let y = IntChoice 42
let z = BoolChoice true

* pattern matching
match booleanExpression without
	| true -> // true branch
	| false -> // false branch

* loops are generally done using recursion

* record types
type Person = {FirstName:string; LastName:string; Dob:DateTime}
type Coord = {Lat:float; Long:float}

* union (choice) types
type TimePeriod = Hour | Day | Week | Year
type Temperature = C of int | F of int
type Appointment = OneTIme of DateTime 
					| Recurring of DateTime list

Unit of Work Pattern
The Unit of Work pattern is used to group one or more operations (usually database operations) into a single transaction or “unit of work”, so that all operations either pass or fail as one. 

public interface IUnitOfWork
{
    void BeginTransaction();
    void Commit();
    void Rollback();
}

Repository Pattern
The Repository pattern is used to manage CRUD operations through an abstract interface that exposes domain entities and hides the implementation details of database access code.					

public interface IRepository<T> where T : IEntity
{
    IQueryable<T> GetAll();
    T GetById(int id);
    void Create(T entity);
    void Update(T entity);
    void Delete(int id);
}



http://jr0cket.co.uk/2016/05/ssh-or-https-that-is-the-github-question.html


https://medium.freecodecamp.org/demystifying-containers-101-a-deep-dive-into-container-technology-for-beginners-d7b60d8511c1
https://medium.freecodecamp.org/a-quick-introduction-to-web-security-f90beaf4dd41
https://hackernoon.com/38-actions-and-insights-to-become-a-better-software-architect-f135e2de9a1b
