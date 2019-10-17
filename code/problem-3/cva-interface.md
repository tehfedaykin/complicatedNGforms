## Implement the CVA Interface

```typescript
import { Component, OnInit, Input, forwardRef } from '@angular/core';
import { ControlValueAccessor, NG_VALUE_ACCESSOR } from '@angular/forms';
import { tap, distinctUntilChanged, map } from 'rxjs/operators';
import { Observable } from 'rxjs';

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
  @Input() data;

  onChange: any = () => { };
  onTouched: any = () => { };

  registerOnChange( fn : any ) : void {
    this.onChange = fn;
  }

  registerOnTouched( fn : any ) : void {
    this.onTouched = fn;
  }

  writeValue(value) {
    this.value = value;
    this.selectDropdown(value);
  }
}

```