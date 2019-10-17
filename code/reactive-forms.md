
```html
<form>
  <label for="name">Name</form>
  <input class="form-control" [formControl]="name">
</form>
```

```typescript
const name = new FormControl('Jennifer');
```