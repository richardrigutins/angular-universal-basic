# Angular Universal SWA basic

Use this repo with to build and customize a new static [Angular Universal](https://angular.io/guide/universal) application with [Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview).

This project was generated with [Angular CLI](https://github.com/angular/angular-cli), using Angular 15.1.

## Useful scripts

### Setup

Run `npm install` to install the dependencies.

### Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

To use server-side rendering on your local system with Universal, run `npm run dev:ssr` instead and navigate to `http://localhost:4200/`. Similarly to the `ng serve` command, the application will automatically reload if you change any of the source files.

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

To build the project with server-side rendering with Universal, run `npm run build:ssr` instead.

### Prerendering

To prerender your application's pages, run `npm run prerender`. The prerendered files will be stored in the `dist/angular-universal-swa-basic/browser` directory.

### Running with the SWA emulator

To run your application with the [Azure Static Web Apps emulator](https://docs.microsoft.com/azure/static-web-apps/local-development), first build the application with `npm run swa:build`. Then, run `npm run swa:start` to start the emulator. The browser will automatically open to the application's URL.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

### Linting

Run `ng lint` to execute the linter.

### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
