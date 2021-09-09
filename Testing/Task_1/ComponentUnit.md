# Component Unit
- Open the _book-card.component.spec.ts_ next to book-card.component.ts.
- Test the class `BookCardComponent` without its template.
- Assert that after initializing the class all properties of `content` default to `"n/a"`.

## Hints

```ts
import { BookCardComponent } from './book-card.component';

describe('BookCardComponent', () => {
  describe('When no content is passed', () => {
    it('defaults to "n/a"', () => {
       // Write your test here, please
    });
  })
});
```
