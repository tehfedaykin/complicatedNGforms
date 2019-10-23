## CVA Template Wrapping 3rd Party Component

```html
<ng-template #itemTemplate let-model="item">
  {{model.name}}
</ng-template>
<input
  class="form-control"
  [(ngModel)]="selected"
  [typeahead]="data"
  typeaheadOptionField="name"
  [typeaheadItemTemplate]="itemTemplate"
  [typeaheadMinLength]="0"
  (typeaheadOnSelect)="onSelect($event)"
  (blur)="onBlur()"
>

```
