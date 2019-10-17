## Build the Wrapper Component

```typescript
import { Component, OnInit, Input, forwardRef } from '@angular/core';
import { ControlValueAccessor, NG_VALUE_ACCESSOR } from '@angular/forms';

@Component({
  selector: 'app-typeahead',
  templateUrl: './type-ahead.component.html',
  styleUrls: ['./type-ahead.component.less'],
  providers: [
    {
      provide: NG_VALUE_ACCESSOR,
      useExisting: forwardRef(() => TypeAheadComponent),
      multi: true
    }
  ]
})
export class TypeAheadComponent implements ControlValueAccessor {
 ...
}

```