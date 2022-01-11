# AngularSendingDataToChild

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.2.8.

## parent.component.ts

    import { Component, OnInit } from '@angular/core';
    @Component({
    selector: 'app-parent',
    template: `<app-child [childMessage]="parentMessage"></app-child>`,
    styleUrls: ['./parent.component.scss']
    })
    export class ParentComponent implements OnInit {
    parentMessage = "message from parent";
    constructor() { }
    ngOnInit(): void { }
    }

## child.component.ts

    import { Component, Input, OnInit } from '@angular/core';
    @Component({
    selector: 'app-child',
    template: `<p> Say {{ childMessage }}</p>`,
    styleUrls: ['./child.component.scss']
    })
    export class ChildComponent implements OnInit {
    @Input() childMessage!: string;
    constructor() { }
    ngOnInit(): void { }
    }
## Development server

Run ng serve for a dev server. Navigate to http://localhost:4200/. The app will automatically reload if you change any of the source files.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

