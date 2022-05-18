
# Angular CheatSheet



### Sections


* [Angular Pipes](https://github.com/thewasiullah/cheatsheets/blob/main/angular.md#angular-pipes)




## Angular Pipes


### Highlight pipe

Pipe to hightlight given text

#### Highlight pipe class
```angular
import { PipeTransform, Pipe } from '@angular/core';

@Pipe({ name: 'highlight' })
export class HighlightPipe implements PipeTransform {
  transform(text: string, search): string {
    if (search && text) {
      let pattern = search.replace(/[\-\[\]\/\{\}\(\)\*\+\?\.\\\^\$\|]/g, '\\$&');
      pattern = pattern.split(' ').filter((t) => {
        return t.length > 0;
      }).join('|');
      const regex = new RegExp(pattern, 'gi');
      return text.replace(regex, (match) => `<span style="background-color: #F2E366;">${match}</span>`);
    } else {
      return text;
    }
  }
}

```

#### Highlight pipe usage
```angular
<div [innerHTML]="item.Content  | highlight: search "></div>
'''

#### ngFor example
```angular
<ul>
  <li *ngFor="let item of items; let i = index">
    {{i}} {{item}}
  </li>
</ul>



<ul>
  <li *ngFor="let item of items">
    {{item}}
  </li>
</ul>
```
<p align="right">(<a href="#top">back to top</a>)</p>

