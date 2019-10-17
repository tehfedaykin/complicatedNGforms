```typescript
import { FormBuilder } from '@angular/forms';
...
export class FormComponent implements OnInit {
  public usersForm;
  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.usersForm = this.fb.array([
      this.fb.group({
        firstName: [{value: '', disabled: false}],
        lastName: [{value: '', disabled: false}],
        email: [{value: '', disabled: false}]
      })
    ]);
  }
}
```