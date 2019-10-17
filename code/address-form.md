```typescript
import { Component, OnInit } from '@angular/core';
import { ControlContainer } from '@angular/forms';

@Component({
  selector: 'app-address',
  template: `
  <form  *ngIf="ogFormGroup" [formGroup]="ogFormGroup">
    <h5>Address:</h5>
    <div class="form-group">
      <label for="name">Street Name</label>
      <input formControlName="street" />
    </div>
    <div class="form-group">
      <label for="name">City</label>
      <input formControlName="city" />
    </div>
    <div class="form-group">
      <label for="name">State</label>
      <input formControlName="state" />
    </div>
    <div class="form-group">
      <label for="name">Zip</label>
      <input formControlName="zip" />
    </div>
  </form>
  `,
  styleUrls: ['./address.component.less']
})
export class AddressComponent implements OnInit {
  public ogFormGroup;
  constructor(public controlContainer: ControlContainer) {
  }

  ngOnInit() {
    this.ogFormGroup = this.controlContainer.control;
  }

}
```