```html
<h3>Personal Information</h3>
<div class="nested-form">
  <div class="form-group">
    <mat-form-field>
      <mat-label for="firstName">First Name</mat-label>
      <input matInput formControlName="firstName" />
    </mat-form-field>
  </div>
  ...
  <button [disabled]="!myControlsValidityHere">Next Step</button>
</div>
```