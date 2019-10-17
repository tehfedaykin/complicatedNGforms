### Async Pipe

Creates a subscription in the template and *unsubscribes* when component is destroyed.

```html
<ul class="queens">
  <li ng-repeat="queen in (displayedQueens$ | async)">
    <a routerLink="queens/{{queen.id}}">{{queen.name}}</a>
    <p>{{queen.quote}}</p>
  </li>
</ul>
```