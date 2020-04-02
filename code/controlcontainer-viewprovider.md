### ViewProvider

```typescript
import { Component, OnInit } from '@angular/core';
import { ControlContainer, FormGroupDirective } from '@angular/forms';

@Component({
  selector: 'app-step1',
  templateUrl: './step1.component.html',
  styleUrls: ['./step1.component.less'],
  viewProviders: [{provide: ControlContainer, useExisting: FormGroupDirective}]
})
export class Step1Component implements OnInit {
  constructor() {}

  ngOnInit() {}
}
```