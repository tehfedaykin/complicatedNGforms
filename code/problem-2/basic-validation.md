## Basic required validation

```typescript
import { FormControl, Validators } from '@angular/forms';

const control = new FormControl('initial value', {validators: Validators.required})
```

We have several built-in validators at our disposal:
<p class="small">min(), max(), required(), requiredTrue(), email(), minLength(),
  <br />maxLength(), pattern(), nullValidator(), compose(),
  composeAsync()</p>