```typescript
import { Component, OnInit } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

@Component({
  selector: 'app-span-form',
  template: `
  <form [formGroup]="sampleForm">
    <div class="form-group">
      <label for="name">First Name</label>
      <input name="first_name" formControlName="first_name" />
    </div>
    <div class="form-group">
      <label for="name">Last Name</label>
      <input name="last_name" formControlName="last_name" />
    </div>
    <div class="form-group">
      <label for="name">Email Address</label>
      <input name="email" formControlName="email" />
    </div>
    <app-address></app-address>
  </form>
  `,
  styleUrls: ['./span-form.component.less']
})
export class SpanFormComponent implements OnInit {
  public sampleForm: FormGroup;
  constructor(
    private fb: FormBuilder
  ) { }

  ngOnInit() {
    this.sampleForm = this.fb.group({
      user_name: ['', Validators.required],
      first_name: ['',Validators.required],
      last_name: ['',Validators.required],
      email: ['',Validators.required],
      street: ['',Validators.required],
      city: ['',Validators.required],
      state: ['',Validators.required],
      zip: ['',Validators.required]
    })
  }

}
```