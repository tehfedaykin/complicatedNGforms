### Observable

A lazy Push collection of multiple values over time. 

```typescript
const {Observable} = rxjs;

const observable = Observable.create(function (observer) {
  observer.next(1);
  observer.next(2);
  observer.next(3);
});

function subscriber( value ){
    console.log('got value ' + value);
    // Logs 1, 2, 3
}

observable.subscribe( subscriber );
```