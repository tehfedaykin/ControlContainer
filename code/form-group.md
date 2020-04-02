### Form Setup

```typescript
this.loanApplication = new FormGroup({
  firstName: new FormControl(
    {value: '', disabled: false},Validators.required
  ),
  lastName: new FormControl(
    {value: '', disabled: false},Validators.required
  ),
  streetNumber: new FormControl(
    {value: '', disabled: false}, Validators.required
  ),
  islandName: new FormControl(
    {value: '', disabled: false}, Validators.required
  ),
  initialDeposit: new FormControl(
    {value: 0, disabled: false}, Validators.required
  ),
  loanType: new FormControl(
    {value: '', disabled: false}, Validators.required
  ),
  roofColor: new FormControl(
    {value: '', disabled: false}, Validators.required
  ),
  friendCode: new FormControl({value: '', disabled: false})
});
```