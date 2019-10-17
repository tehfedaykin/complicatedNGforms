## Function Validation

```typescript
amountValidator(control: FormControl) {
  return control.value > 340 ? null : {
    validAmount: {
      valid: false
    }
  }
}

const control = new FormControl('some value', {
  validators: [Validators.required, amountValidator]
})
```