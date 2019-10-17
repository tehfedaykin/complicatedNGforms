### Working with Operators

```typescript
import { mergeMap } from  'rxjs/operators';

this.allQueens$ = this.QueenService.getQueens();

this.displayedQueens$ = this.selectedSeason.pipe(
  mergeMap((seasonId: string) => {
    if (seasonId) {
      return this.QueenService.getSeasonQueens(seasonId) as Observable<IQueen[]>;
    }
    else {
      return this.allQueens$ as Observable<IQueen[]>;
    }
  })
)
```
