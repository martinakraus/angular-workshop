# Effects III

- Implement the feature "Update Book" using the NgRx infrastructure.
- Implement the feature "Delete Book" using the NgRx infrastructure.

## Hints

```ts
export const deleteBookStart = createAction('[Book] Delete Book Started');
export const deleteBookComplete = createAction('[Book] Delete Book Completed', props<{ bookIsbn: string }>());

export const updateBookStart = createAction('[Book] Update Book Started', props<{ patch: Book }>());
export const updateBookComplete = createAction('[Book] Update Book Completed', props<{ update: Book }>());
```

[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-use-effects-everywhere)
