```typescript
import { Component, OnInit } from '@angular/core';
import { FormControl } from '@angular/forms';

@Component({
  selector: 'my-form',
  template: `<input type="text" [formControl]="myControl" />`,
  styleUrls: ['./app.component.less']
})
export class FormComponent {
  public myControl = new FormControl('initial value');
}
```

<p class="small">Any piece of information we want to collect in a form, whether it's an input, select, dropdown, or custom element needs to have a representative FormControl. The `[formControl]` directive is used to bind the input element in the DOM to its respective FormControl.</p>
