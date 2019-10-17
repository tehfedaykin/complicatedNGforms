## My Preferred Validation

```css
.form-group {
  .ng-valid[required], .ng-valid.required  {
    border-left: 5px solid #42A948; /* green */
  }
  .ng-touched.ng-invalid:not(form) {
    border-left: 5px solid #a94442; /* red */
  }
}
```

I like to highlight as the user touches fields, but then highlight required untouched fields on save.