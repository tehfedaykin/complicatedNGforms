
```html
<form>
  <label for="name">Name</form>
  <input class="form-control" [formControl]="name">
</form>
```

```typescript
public name: FormControl = new FormControl({value: 'Jennifer'}, Validators.required);
```