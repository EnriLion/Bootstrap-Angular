# Bootstrap-Angular
**This repository is to create an easy script with Poweshell and Bash to get this configuration easily.**

First you need to create your project

```
ng new app
```

After that we need to install the classic way using npm in your project

```
npm install bootstrap
```

There are plenty of information that the only way is using sass but you could achieved as well as using the classic css

**Write this lines in your angular.json**

```
            "styles": [
              "node_modules/bootstrap/scss/bootstrap.scss",
              "node_modules/bootstrap-icons/font/bootstrap-icons.css",
              "src/styles.scss"
            ],
            "scripts": [
              "node_modules/bootstrap/dist/js/bootstrap.bundle.min.js"
            ]
```

After that is where the things are more complicated, there are problems with compability for that reason we need to install other ng component: 

```
 ng add @ng-bootstrap/ng-bootstrap@next 
```

It's almost done, don't worry for that.
Look and verify if your module is loaded in typescript you could import it(app.module.ts)
```
 import { NgbModule } from '@ng-bootstrap/ng-bootstrap';
```
Also in the same file you need to import it
```
    NgbModule
```
And the final step verify as well in your component app.component.ts( its the same line of "import" as the previous one)
In that file  you need to add inside the export class AppComponent:
```
export class AppComponent {
  title = 'aplicacion';
  constructor(private modalService: NgbModal) {
  }

  public open(modal: any): void {
    this.modalService.open(modal);
  }
}
```
