## FormArray Markup

```html
<div class="form-group" *ngIf="lipsyncs$ | async as lipsyncs">
  <label for="favorite_queen">Choose A Few Favorite Lipsyncs</label>
  <ng-container *ngFor="let lipSyncGroup of lipSyncFormArray.controls; let i=index">
    <div class="form-group" [formGroup]="lipSyncGroup">
      <app-typeahead formControlName="lipsync" [data]="lipsyncs"></app-typeahead>
      <input type="text" formControlName="ranking" />
      <button (click)="removeLipsync(i)">X</button>
    </div>
  </ng-container>
  <button (click)="addLipsync()">Add another lipsync</button>
</div>
```