```typescript
import { Component, OnInit } from '@angular/core';
import { FormControl, FormGroup } from '@angular/forms';

@Component({
  selector: 'my-form',
  template: `
    <form [formGroup]="myForm">
      <label>First Name:</label><input formControlName="firstName" />
      <label>Last Name:</label><input formControlName="lastName" />
      <label>Email:</label><input formControlName="email" />
    </form>
  `,
  styleUrls: ['./app.component.less']
})
export class FormComponent {
  public myForm = new FormGroup({
    firstName: new FormControl('', {}),
    lastName: new FormControl('', {}),
    email: new FormControl('', {})
  });
}
```