### Behavior Subject 

Similar to a Subject but will re-emit the last emitted value(or default value if set)

```typescript
const {BehaviorSubject} = rxjs;

var subject = new BehaviorSubject<String>();

subject.next("THE PAST");

subject.subscribe((value) => console.log(value));
// logs "THE PAST"
```