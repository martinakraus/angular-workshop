# Component Mock Dependency
- Open _book.component.spec.ts_ next to book.component.ts, if the file not exists.
- Create a mock for `BookApiService` with Jasmine.
- Configure the mock returning one Book when method `getAll` ist called.
- You need to import the `RouterTestingModule` in order to have the component created
- You need to decklare all dependencies (ChildComponents and FilterPipes) inside you TestingModule
- Assert that three books are emited through the `books$` Observable.

## Hints

```ts
// Create Mock    
bookApiMock = jasmine.createSpyObj<BookApiService>(['getAll']);

// Custom Provider for TestBed
{
    provide: BookApiService,
        useValue: bookApiMock
}

// Configure mock    
bookApiMock.getAll.and.returnValue(of([bookNa(), bookNa()]));
```
