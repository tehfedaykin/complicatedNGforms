Initially subcategory is unrequired

```typescript
this.mainForm = this.fb.group({
  ...
  favorite_queen: ['80',Validators.required],
  favorite_season: ['',Validators.required],
  favorite_episode: ['']
})
```