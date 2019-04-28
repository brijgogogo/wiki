= routing =
a route maps to a component
routes follow first match strategy

# showing routes
<a routerLink="/items">Items</a>
<a [routerLink]="['/home']">Home</a>

# route definition:
{ path: 'items', component: ItemListComponent }

# location of display of route component:
<router-outlet></router-outlet>

# router module
import { RouterModule } from '@angular/router';

@NgModule({
  imports: [
    RouterModule.forRoot([]) // pass array of route definitions
    //RouterModule.forRoot([], { useHash: true }) //for hash routes
  ]
})


# index.html
<base href="/">
tells the router how to compose the navigation urls


# route definition examples
{ path: 'items', component: ItemListComponent }

//route paramters
{ path: 'items/:id', component: ItemDetailComponent }

//redirect
{ path: 'home', component: HomeComponent}
{ path: '', redirectTo: 'home', pathMatch: 'full' }

//wildcard path
{ path: '**', component: PageNotFoundComponent }

