## Add To Form

Use FormArray `insert` method

```typescript
addLipsync() {
  let length = this.lipSyncFormArray.controls.length;
  this.lipSyncFormArray.insert(length, new FormGroup({
    lipsync: new FormControl(''),
    ranking: new FormControl('0')
  }))
}
```