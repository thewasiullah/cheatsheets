
# Angular CheatSheet



### Sections


* [Angular Pipes](https://nextjs.org/)

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

