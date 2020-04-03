```html
<h3>Personal Information</h3>
<div [formGroup]="controlContainer.control" class="nested-form">
  <div class="form-group">
    <mat-form-field>
      <mat-label for="firstName">First Name</mat-label>
      <input matInput formControlName="firstName" />
    </mat-form-field>
  </div>
  ...
  <button [disabled]="!controlContainer.control.get('firstName').valid">Next Step</button>
</div>
```
<p class="small">In this case we do need to assign the control (our FormGroup) in the ControlContainer provider to the formGroup directive.</p>