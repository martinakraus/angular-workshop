# Test | Mock Selector

- Open _book.component.spec.ts_.
- Use `provideMockStore()` for `providers[]` inside out TestBed Module
- Use the overriderSelector Function to mock the selector for `bookCollection`
- 
> _Ressource: [NgRx Testing](https://ngrx.io/guide/store/testing#using-mock-selectors)_

## Hints

```ts
import { MockStore, provideMockStore } from '@ngrx/store/testing';

providers: [provideMockStore()],

store = TestBed.inject(MockStore);
store.overrideSelector(bookCollection as any, [new BookNa()]);
```
[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-testing-selector-with-bonus)
