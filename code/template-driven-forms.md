```typescript
const model = {
  name: '',
  age: '',
  ...
};
```

```html
<form>
  <label for="name">Name</form>
  <input class="form-control" name="name" [(ngModel)]="model.name">
</form>
```

