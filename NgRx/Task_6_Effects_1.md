# Effects I

- Install _@ngrx/effects_ by executing `ng add @ngrx/effects`.
- Check if the installation was successful by having a look at _app.module.ts_.
    - You should see _EffectsModule.forRoot([])_

- Open _book/store/book-collection.actions.ts_
- Create the action `loadBookStart`, being used to send a GET-Request to the API.
- Create the action `loadBookComplete`, being used to react to the response of the API.

- Create the file _book/store/book-collection.effects.ts_ `ng generate effect book-collection`
- Implement the effect `load` that uses _BookApiService_ to load all books.
- Return the action `loadBookComplete`, when the books have been loaded successfully.
- Register _BookCollectionEffects_ in _book.module.ts_ by adding `EffectsModule.forFeature([BookCollectionEffects])`.

- Open _book/store/book-collection.reducer.ts_.
- Update the reducer function handling the action `loadBookComplete`.
    - It should save the books coming from the API to the store.

- Open _book.component.ts_.
- Dispatch the action `loadBookStart` triggering the GET-Request loading all books.

- Visit your app again.
- Check if the books are loaded instantly when you visit the book list.

## Hints

```typescript
// actions
export const loadBooksStart = createAction('[Book] Load Books Started');
export const loadBooksComplete = createAction('[Book] Load Books Completed', props<{ books: Book[] }>());
```

[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-introduce-effects)
