## Form with FormArray

```typescript
    this.mainForm = this.fb.group({
      ...
      favorite_lipsyncs: this.fb.array([
        this.fb.group({
          lipsync: [''],
          ranking: ['']
        })
      ])
    })
```