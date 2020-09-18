## AbstractControl

```typescript
abstract class AbstractControl {
  constructor(validators: ValidatorFn | ValidatorFn[], asyncValidators: AsyncValidatorFn | AsyncValidatorFn[])
  value: any
  validator: ValidatorFn | null
  asyncValidator: AsyncValidatorFn | null
  parent: FormGroup | FormArray
  status: string
  valid: boolean
  invalid: boolean
  pending: boolean
  disabled: boolean
  enabled: boolean
  errors: ValidationErrors | null
  pristine: boolean
  dirty: boolean
  touched: boolean
  untouched: boolean
  valueChanges: Observable<any>
  statusChanges: Observable<any>
  updateOn: FormHooks
  root: AbstractControl
  setValidators(newValidator: ValidatorFn | ValidatorFn[]): void
  setAsyncValidators(newValidator: AsyncValidatorFn | AsyncValidatorFn[]): void
  clearValidators(): void
  clearAsyncValidators(): void
  markAsTouched(opts: { onlySelf?: boolean; } = {}): void
  markAllAsTouched(): void
  markAsUntouched(opts: { onlySelf?: boolean; } = {}): void
  markAsDirty(opts: { onlySelf?: boolean; } = {}): void
  markAsPristine(opts: { onlySelf?: boolean; } = {}): void
  markAsPending(opts: { onlySelf?: boolean; emitEvent?: boolean; } = {}): void
  disable(opts: { onlySelf?: boolean; emitEvent?: boolean; } = {}): void
  enable(opts: { onlySelf?: boolean; emitEvent?: boolean; } = {}): void
  setParent(parent: FormGroup | FormArray): void
  abstract setValue(value: any, options?: Object): void
  abstract patchValue(value: any, options?: Object): void
  abstract reset(value?: any, options?: Object): void
  updateValueAndValidity(opts: { onlySelf?: boolean; emitEvent?: boolean; } = {}): void
  setErrors(errors: ValidationErrors, opts: { emitEvent?: boolean; } = {}): void
  get(path: string | (string | number)[]): AbstractControl | null
  getError(errorCode: string, path?: string | (string | number)[]): any
  hasError(errorCode: string, path?: string | (string | number)[]): boolean
}
```
