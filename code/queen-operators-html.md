### Working with Operators

```html
<select name="" id="" ng-model="vm.season" 
ng-change="vm.selectedSeason.next(vm.season)">
  <option value="">Select Season</option>
  <option value="{{season.id}}" 
  ng-repeat="season in (vm.seasons$ | async:this)">
    Season {{season.seasonNumber}}
  </option>
</select>
<label for="winners">Only show winning queens:</label>
<ul class="queens">
  <li ng-repeat="queen in (vm.displayedQueens$ | async:this)">
    <a href="#!/queens/{{queen.id}}">{{queen.name}}</a>
    <p>{{queen.quote}}</p>
  </li>
</ul>
```
