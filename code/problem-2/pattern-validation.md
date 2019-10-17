## Pattern Validation

```typescript
const control = new FormControl('initial value', {
  validators: Validators.pattern('[0-9]{5}')
})

const mySpecificallyNamedPattern = "^\\d{2}\/\\d{2}\/\\d{4}$";
const otherControl = new FormControl('10-15-2019', {
  validators: Validators.pattern(mySpecificallyNamedPattern)
})
```