
# Angular CheatSheet



### Sections


* [Angular Pipes](https://github.com/thewasiullah/cheatsheets/main/angular.md#angular-pipes)

<p align="right">(<a href="#top">back to top</a>)</p>



### Angular Pipes


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

