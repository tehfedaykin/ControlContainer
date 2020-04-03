### Step 1 Component

```html
<h3>Personal Information</h3>
<div class="nested-form">
  <div class="form-group">
    <mat-form-field>
      <mat-label for="firstName">First Name</mat-label>
      <input matInput formControlName="firstName" />
    </mat-form-field>
  </div>
  <div class="form-group">
    <mat-form-field>
      <mat-label for="lastName">Last Name</mat-label>
      <input matInput formControlName="lastName" />
    </mat-form-field>
  </div>
  <h4>Wanna be Social? Add Your Friend code!</h4>
  <p>(Read about how to find your friend code 
    <a target="_blank" href="https://nintendo.com">here</a>)
  </p>
  <div class="form-group">
    <app-switch-code formControlName="friendCode"></app-switch-code>
  </div>
  <app-address-fields></app-address-fields>
</div>
```