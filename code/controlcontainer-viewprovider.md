```typescript
@Component({
  selector: 'app-step1',
  templateUrl: './step1.component.html',
  styleUrls: ['./step1.component.less'],
  viewProviders: [{provide: ControlContainer, useExisting: FormGroupDirective}]
})
export class Step1Component implements OnInit {
  ...
```
<p class="small">We can inject the ControlContainer into just our child component by providing it in the ViewProviders option.</p>
