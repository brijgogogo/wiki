= pipes =
Transform bound properties before display


== built-in pipes ==
* date
* nubmer, decimal, percent, currency
* json, slice


%% {{ product.productCode | lowercase }}
<img [title]='product.productName | uppercase'>

chaining pipes
%% {{ product.price | currency | lowercase }}

pipes with paramters
%% {{ product.price | currency:'USD':'symbol':'1.2-2' }}
currency pipe has 3 paramters: desired currency code, a string defining how to show the currency symbol, and digit info
1.2-2 : at least one digit to the left of decimal, at least one digit to the right of the decimal, and no more than two digits to the right of decimal digit.

== custom pipes ==
* defining a pipe
import { Pipe, PipeTransform } from '@angular/core';
@Pipe({
  name: 'convertToSpaces'
})
export class ConvertToSpacesPipe implements PipeTransform {
  transform(value: string, character: string): string {
    //value is the value on which transform is to be applied
    //rest are arguments
    return "";
  }
}

* using a pipe
%%<td>{{ obj.Name | convertToSpaces:'-' }}<td>

* declaring in the Module
@NgModule({ declarations: [ ConvertToSpacesPipe ] })
export class AppModule {  }
