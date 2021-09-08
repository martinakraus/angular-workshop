# Test | Mock Selector

- Open _book-list.component.spec.ts_.
- Fix the failing test.
- Replace the _BookApiService_-Mock with a Selector-Mock.

> _Ressource: [NgRx Testing](https://ngrx.io/guide/store/testing#using-mock-selectors)_

## Hints

```ts
import { MockStore, provideMockStore } from '@ngrx/store/testing';

providers: [provideMockStore()],

store = TestBed.inject(MockStore);
store.overrideSelector(bookCollection as any, [new BookNa()]);
```
[Solution](https://stackblitz.com/github/workshops-de/angular-advanced-workshop/tree/solve--ngrx-testing-selector-with-bonus)
