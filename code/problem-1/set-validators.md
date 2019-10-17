## Step Two

Get dependent formControl and use `setValidators` method.

```typescript
this.mainForm.get('favorite_season').valueChanges.subscribe((val) => {
  const favEpControl = this.mainForm.get('favorite_episode');
  if(val) {
    favEpControl.setValidators(Validators.required);
  }
  else {
    favEpControl.setValidators(null)
  }
})
```