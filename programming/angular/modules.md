= module =

An Angular application comprises of separate modules which are closely related
blocks of functionality. Every Angular application has at least one module:
the root module (mostly named `AppModule`).

import { BrowserModule } from '@angular/platform-browser'
import { NgModule } from '@angular/core';
import { FormModule } from '@angular/forms';
import { HttpModule } from '@angular/http';

import { AppComponent } from './app.component';

@NgModule({
declarations: [
  AppComponent
],
imports: [
owserModule,
FormsModule,
HttpModule
],
providers: [],
bootstrap: [AppComponent]
})
export class AppModule {  }

A `module` is a plain TypeScript class with the @`NgModule` decorator. The
decorator tells Angular that this class is going to be a module. This
decorator adds metadata above this class. In the decorator are array
attributes which Angular looks for in a module class:

`declarations` - to declare which components, directives or pipes are in this
module.

`imports` - to specify what other modules do we use for this module.

`providers` - to specify any application wide services we want to use.

