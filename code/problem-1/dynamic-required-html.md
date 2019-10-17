Let's say we only want the favorite episode
field to be required if favorite season has a value

```html
<div class="form-group">
  <label for="name">Season</label>
  <select name="season" formControlName="favorite_season">
    <option value="{{season.id}}" *ngFor="let season of (seasons$ | async)">
      Season {{season.seasonNumber}}
    </option>
  </select>
</div>
<div class="form-group">
  <label for="name">Episode</label>
  <select name="episode" formControlName="favorite_episode">
    <option value="{{episode.id}}" *ngFor="let episode of (episodes$ | async)">
      {{episode.title}}
    </option>
  </select>
</div>
```