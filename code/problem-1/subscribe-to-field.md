## Step One

Subscribe to changes on the field that determines other fields' requiredness

```typescript
this.mainForm.get('favorite_season').valueChanges.subscribe((val) => {
  console.log(`Favorite season changed to: ${val}`);
})
```