# AngularPaginatorGuru

A simple and highly customizable plug-n-play package for pagination in Angular (v2+)

## Quick Start

```sh
$ npm install angular-paginator-guru
```

## Sample Implementation

```sh
// app.module.ts
import {NgModule} from '@angular/core';
import {BrowserModule} from '@angular/platform-browser';

import {PaginatorModule} from 'angular-paginator-guru'; // <-- import the module
import {MyComponent} from './my.component';
 
@NgModule({
    imports: [BrowserModule, PaginatorModule], // <-- include it in your app module
    declarations: [MyComponent],
    bootstrap: [MyComponent]
})
export class MyAppModule {}
```

```sh
// my.component.ts
import {Component} from '@angular/core';
 
@Component({
    selector: 'my-component',
    template: `
    <ul>
      <li *ngFor="let item of collection"> ... </li>
    </ul>
               
    <app-paginator-guru 
        (PageChange)="onPageChange($event)" 
        totalItemsCount=90 
        itemsPerPage=10>
    </app-paginator-guru>
    `
})
export class MyComponent {
    collection: any[] = someArrayOfThings;  
    
    onPageChange(currentPage) {
        // Fetch data based on currentPage and update collection
        // console.log(currentPage)
  }
}
```