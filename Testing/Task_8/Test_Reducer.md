# Test | Reducer

- Create the file _book/store/book-collection.reducer.spec.ts_
- Write a test ensuring that action `bookCreateComplete` adds a book to the store.

> _This task contains a bonus part._

## Hints

```ts
const initialState: EntityState<Book> = { entities: {}, ids: [] };
const action = createBookComplete({ book });
const state = bookCollectionReducer(initialState, action);
```

## Bonus

- Write tests for every action handled by `bookCollectionReducer`.

[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-testing-reducer)
