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
