```typescript
import { Component, OnInit } from '@angular/core';
import { FormControl, FormGroup, FormArray } from '@angular/forms';

@Component({
  selector: 'my-form',
  template: `
    <form [formGroup]="usersForm">
      <ng-container *ngFor="let userFormGroup of usersForm.controls;">
        <div [formGroup]="userFormGroup">
          <label>First Name:</label><input formControlName="firstName" />
          <label>Last Name:</label><input formControlName="lastName" />
          <label>Email:</label><input formControlName="email" />
        </div>
      </ng-container>
    </form>
  `,
  styleUrls: ['./app.component.less']
})
export class FormComponent {
  public usersForm = new FormArray([
    new FormGroup({
      firstName: new FormControl('', {}),
      lastName: new FormControl('', {}),
      email: new FormControl('', {})
    }),
    new FormGroup({
      firstName: new FormControl('', {}),
      lastName: new FormControl('', {}),
      email: new FormControl('', {})
    })
  ]);
}
```