### Form HTML

```html
<form [formGroup]="loanApplication" class="loan-form">
  <mat-form-field>
    <mat-label for="firstName">First Name</mat-label>
    <input matInput formControlName="firstName" />
  </mat-form-field>
  <mat-form-field>
    <mat-label for="lastName">Last Name</mat-label>
    <input matInput formControlName="lastName" />
  </mat-form-field>
  <h4>Wanna be Social? Add Your Friend code!</h4>
  <p>(Read about how to find your friend code 
    <a target="_blank" href="https://nintendo.com">here</a>)</p>
  <app-switch-code formControlName="friendCode"></app-switch-code>
  <mat-form-field>
    <mat-label for="streetNumber">Street</mat-label>
    <input matInput formControlName="streetNumber" />
  </mat-form-field>
  <mat-form-field>
    <mat-label for="islandName">Island</mat-label>
    <input matInput formControlName="islandName" />
  </mat-form-field>
  <mat-form-field>
    <mat-label>Loan Type</mat-label>
    <mat-select formControlName="loanType">
      <mat-option *ngFor="let loanType of loanTypes$ | async" [value]="loanType" >
        {{loanType.type}}
      </mat-option>
    </mat-select>
  </mat-form-field>
  <mat-form-field>
    <mat-label>Roof Color</mat-label>
    <mat-select formControlName="roofColor">
      <mat-option *ngFor="let color of roofColors" [value]="color">
        {{color}}
      </mat-option>
    </mat-select>
  </mat-form-field>
  <label for="initialDeposit">Deposit</label>
  <p>{{sliderValue$ | async | number:'.2'}} Bells</p>
  <mat-slider color="primary" min="1" value="0" formControlName="initialDeposit"
  [max]="loanApplication.controls.loanType.value.loanAmount"
   (input)="sliderValue$.next($event.value)"></mat-slider>
  <div class="form-group">
    <p>Remaining Amount Due: {{ remainingBalance$  | async | number:'.2' }} Bells</p>
  </div>
</form>
```