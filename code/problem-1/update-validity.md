## Step Three

Update changed formControls validity.

```typescript
this.mainForm.get('favorite_season').valueChanges.subscribe((val) => {
  const favEpControl = this.mainForm.get('favorite_episode');
  if(val) {
    favEpControl.setValidators(Validators.required);
  }
  else {
    favEpControl.setValidators(null)
  }
  favEpControl.updateValueAndValidity();
})
```