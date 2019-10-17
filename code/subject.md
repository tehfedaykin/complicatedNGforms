### Subject

A special type of Observable that can be multicasted to many observers. A subject can both published and be subscribed to.

```typescript
const {Subject} = rxjs;
const subject = new Subject<number>();

subject.subscribe({
  next: (v) => console.log(`observerA: ${v}`)
});
subject.subscribe({
  next: (v) => console.log(`observerB: ${v}`)
});

subject.next(Math.random());
subject.complete();
```