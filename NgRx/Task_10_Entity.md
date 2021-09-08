# Entity

- Install NgRx Entity by executing `ng add @ngrx/entity`.
- Update the interface `BookCollectionSlice` to extend `EntityState<Book>`.
- Update the reducer `bookCollectionReducer` using the _EntityAdapter_-Methods _getInitialState, addOne, updateOne, removeOne, setAll_.
- Use the selector `selectAll` of the entityAdapter for the selector `bookCollection`
## Hints

```ts
// book-collection.slice.ts
export type BookCollectionSlice = EntityState<Book>;

// book-collection.reducer.ts
const adapter = createEntityAdapter<Book>({ selectId: model => model.isbn });
```

[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-use-entity)
