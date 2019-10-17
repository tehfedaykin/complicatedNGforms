## What if...

an option was supposed to be preselected based on data?

```typescript
this.mainForm.get('favorite_season').valueChanges.subscribe((val) => {
  const favEpControl = this.mainForm.get('favorite_episode');
  favEpControl.setValue('59');
})
```