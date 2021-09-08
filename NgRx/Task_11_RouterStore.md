# RouterStore

- Install the RouterStore by executing `ng add @ngrx/router-store`
- Register the RouterStore's reducer in _app.module.ts_: `StoreModule.forRoot({ router: routerReducer }, { /* ... */ })`
- Create the file _app/store/router/router.selectors.ts_
- Reexport all RouterStore's selctors (see: [NgRx Docs | Selectors](https://ngrx.io/guide/router-store/selectors))

- Open _book/store/book-collection.selectors.ts_
- Update `bookByIsbn` to use the RouterStore's selector `selectRouteParam('isbn')`
    - Therefore you need to compose two selectors: _bookCollection & selectRouteParam_
    - This means `bookByIsbn` no longer takes a parameter because we now get the route parameter from the Store.
- Update all usages of `bookByIsbn`
- Remove the `ActivatedRoute`-Service from the respective components.

> _Notice that each component that is fully migrated has only one dependency, the Store._

## Hints

__Replace relative import paths with path-alias__

- Create a barrel file (index.ts) inside _app/store/router_.
- Make the barrel file export router-store-related files.
- Open the root-_tsconfig.json_.
- Add the path alias __@store/router__ that points to _./src/app/store/router/index_.
- Update relevant import-paths.

```json
"paths": {
  "@store/router": ["./src/app/store/router/index"]
}
```

[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-use-router-store)
