```typescript
@Component({
  selector: 'app-new-loan',
  templateUrl: './new-loan.component.html',
  styleUrls: ['./new-loan.component.less'],
  providers: [{provide: ControlContainer, useExisting: FormGroupDirective}]
})
export class NewLoanComponent implements OnInit {
  ...
```
<p class="small">We make the ControlContainer available to <span class="accent">all our child components</span> by providing it in the Providers option.</p>
