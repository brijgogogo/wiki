= binding =

== interpolation ==
One way binding from class property to template.
Syntax between double curly braces is called Template Expression. Angular evaluates the expression with component(class) as the context.

examples:
%% <h1>{{pageTitle}}</h1>
%% {{'Title': + pageTitle}}
%% {{2*20+1}}
%% {{'Title: ' + getTitle()}}
%% <h1 innerText={{pageTitle}}></h1>
%% {{showImage ? 'Hide' : 'Show'}} Image


== property binding ==
allows us to set property of an element to the value of a template expression
<img [src]='product.imageUrl'>
binding target is enclosed in square brackets
binding source is enclosed in quotes

<img [style.width.px]='imageWidth'
  [style.margin.px]='imageMargin'>

%%<img src={{product.imageUrl}} : this is interpolation
Interpolation is a special syntax that Angular converts into property binding. It’s a convenient alternative to property binding.

To set an element property to a non-string data value, you must use property binding.
<button [disabled]='isDisabled'>

When we need to concatenate strings we have to use interpolation instead property binding.
%%<img src=' https://angular.io/{{imagePath}}'/>

https://stackoverflow.com/questions/39112904/property-binding-vs-attribute-interpolation

== event binding ==
<button (click)='toggleImage()'>
Target Event is enclosed in parenthesis
On the right of equals is Template Statement in quotes

DOM events can be found at https://developer.mozilla.org/en-US/docs/Web/Events

== two way binding ==
Template <----> Class
<input [(ngModel)]='listFilter'>
Square brackets: indicates property binding
Parenthesis : indicates event binding, to send user entered data notification back to the property

ngModel directive is part of `FormsModule` in @angular/forms
