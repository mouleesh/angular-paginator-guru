# AngularPaginatorGuru

A simple and highly customizable plug-n-play package for pagination in Angular (v2+)

## Quick Start

```sh
$ npm install angular-paginator-guru
```

## Sample Implementation

```sh
// app.module.ts
import {PaginatorModule} from 'angular-paginator-guru'; // <-- import the module

@NgModule({
    imports: [BrowserModule, PaginatorModule], // <-- include it in your app module
})
```

```sh
<app-paginator-guru 
    (PageChange)="onPageChange($event)" 
    totalItemsCount=90 
    itemsPerPage=10>
</app-paginator-guru>

onPageChange(currentPage) {
    // Fetch data based on currentPage and update collection
    // console.log(currentPage)
}
```

## License

MIT
