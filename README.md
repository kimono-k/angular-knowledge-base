# MyFirstApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.2.6.

# How to install Angular

npm install -g @angular/cli@latest

# How to make a starting project

ng new my-dream-app --no-strict

# serve

- ng serve
- http://localhost:4200/

# Add Bootstrap to Angular

- npm i bootstrap
- angular.json
- "styles": [
  node_modules/bootstrap/dist/css/bootstrap.min.css",
  "src/styles.css"
  ],

# Create Components

- ng generate component servers
- check app.module.ts and declare your component

# Component Structure

selector: 'app-root', // this is the self-made html tag
templateUrl: './app.component.html', // the actual html
styleUrls: ['./app.component.css'], // the actual css

# Self-made HTML tag as attribute

selector: '[app-servers]', // html attribute
selector: '.app-servers', // html class

# Self-made HTML tag as class

# HTML

app.component.html

# CSS

- Don't have to rel stylesheet.
- app.component.css automatically adds styles to html.

# Styling Elements Dynamically with ngStyle

- ngStyle gives behaviour when styling (css) should occur.
- <p [ngStyle]="{ backgroundColor: getColor() }">
    {{ "Server" }} with ID {{ serverId }} is {{ getServerStatus() }}
  </p>
- // if online green color, if not red when offline
  getColor() {
  return this.serverStatus === 'online' ? 'green' : 'red';
  }

# Applying CSS Classes Dynamically with ngClass

- ngClass allows us to dynamically (behaviourally) add or remove CSS classes.
- ngClass gives behaviour for specific css classes when the styling should occur.
- ngClass only adds a CSS class if a certain condition is true.
- styles: [
  `
  .online {
  color: white;
  }
  `,
  ],
- <p
  [ngStyle]="{ backgroundColor: getColor() }"
  [ngClass]="{ online: serverStatus === 'online' }"

# Outputting Lists with ngFor

- for of loop in your html
- servers = ['Testserver', 'Testserver 2'];
- <!-- Loops through servers array -->
  <app-server \*ngFor="let server of servers"></app-server>
- onCreateServer() {
  this.serverCreated = true;
  this.servers.push(this.serverName); // push servername into servers array
  this.serverCreationStatus = 'Server was created! ' + this.serverName;
  }

# Planning the App (Recipe book, shopping list app)

- Root component
- Header
- Shopping list (feature)
  - Shopping List
  - Shopping List Edit
- Recipe book (feature)
  - Recipe List
  - Recipe Item
  - Recipe Detail (detail page)

# Attributes directives

- Only change the element they were placed on.

# Global CSS Styles

- In case messy CSS dump everything in styles css in the src folder.

# Where to store images in Angular

![image](https://user-images.githubusercontent.com/34915099/157987109-10236904-4f75-437b-a5bb-d302db60f9b8.png)

![image](https://user-images.githubusercontent.com/34915099/157987536-80bb3c9f-a3d3-4714-82e0-5de9d4cb4b94.png)

![image](https://user-images.githubusercontent.com/34915099/157987558-78541b2b-fc54-4e42-9ffb-a5d94eb72b16.png)

# TS

- app.component.ts there are inline or outline html
- selector: '[app-servers]', // html attribute
  template: ` <app-server></app-server> <app-server></app-server>`,

# TS Getters

// Getter
getServerStatus() {
return this.serverStatus;
}

# Databinding

- Communication between TypeScript (business logic) and HTML (template)

# React to (User) Events

- Click listener HTML -> Typescript
- Event binding

# Event Binding

- (event)="expression"

# Two-way Binding

- [(ngModel)="data"]

# String Interpolation

- {{ data }}
- You can also use strings or functions that return strings.
- {{ "Server" }}
- {{ getServerStatus() }}

# Property Binding

- To make HTML attributes work dynamically (behaviour).
- e.g. bool value
- In template (HTML) [disabled]="!allowNewServer" ! means you want to enable it (the switch to true should be in the constructor).
- allowNewServer = false;
- settimeout 2sec then true;
- [property]="data"
- You can pick property binding or string interpolation.

# Property Binding vs String Interpolation

- DON'T MIX PROPERTY BINDING AND STRING INTERPOLATION.
- Property Binding: If you want to change an HTML attribute dynamically.
- String interpolation: When you want output text.

# Event Binding

- Is interesting for click events
- <button
  class="btn btn-primary"
  [disabled]="!allowNewServer"
  (click)="onCreateServer()"
- x.component.ts needs a handler for the event e.g. onCreateServer()

# Passing and Using Data with Event Binding

- $event = event object access
- event object
- <input type="text" class="form-control" (input)="onUpdateServerName($event)" />
  onUpdateServerName(event: Event) {
  this.serverName = (<HTMLInputElement>event.target).value; // what the user entered
  }
-

# Two-Way-Databinding

- Saves input and output
- [(ngModel)]="serverName"
- Input value stays saved in text field.
- Is like real-time update of the variable.

# What are Directives?

- Instructions in the DOM.
- Components are instructions in the DOM.
- <x></x> in this place
- <p appTurnGreen>Receives a green background!</p>
- @Directive decorator where you create the selector and create the logic inside the class.

# ngIf

- To output data on basis of if/else statements
- A structural directive
- Like a lightbulb it is off then turn it down with the button then show content.
- <p *ngIf="serverCreated">Server was created, server name is {{ serverName }}</p>
- Add or not add in the DOM.

# ngIf with Else

- <!-- When the lightbulb is off perform else case -->
- <p *ngIf="serverCreated; else noServer">
  Server was created, server name is {{ serverName }}
  </p>
- <!-- The else case that should run -->
  <ng-template #noServer>
    <p>No server was created!</p>
  </ng-template>

# Structural Directive

- Changes the structure of the DOM
- It adds this element or doesn't add it

# Combining all Forms of Databinding

# Where To Store Data

- x.component.ts
- // Normally data is coming from HTTP request / database / calculation
  export class ServerComponent {
  girlfriend: "Karina";
  }
- Use data in html template

# Pros of Angular

# Cons of Angular

- Large project folder -> Moving or copying folders just takes too long, make sure the installation path is correct.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
