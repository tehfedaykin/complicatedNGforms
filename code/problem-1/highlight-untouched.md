## Highlight untouched fields

Angular 8:

```typescript
this.mainForm.markAllAsTouched();
```

Angular 7:

```typescript
Object.keys(this.mainForm.controls).forEach((field) => {
  const control = this.mainForm.get(field);
  control.markAsTouched();
})
```