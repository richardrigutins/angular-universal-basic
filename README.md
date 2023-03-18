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

## Developing inside a container

This repo contains a [devcontainer](https://code.visualstudio.com/docs/remote/containers) configuration that can be used to develop the application in a container. To use the devcontainer, you must have [Docker](https://www.docker.com/) and [Visual Studio Code](https://code.visualstudio.com/) installed. Then, open the repo in Visual Studio Code and follow the prompts to reopen the repo in a container. The devcontainer will install the necessary dependencies and extensions for the application.

To launch the application in the devcontainer, run `ng start:devcontainer`. The application will be available at `http://localhost:4200/`.

## Deploying to Azure Static Web Apps

### Using GitHub Actions

This repository contains a GitHub Actions workflow template that can be used to deploy the application to Azure Static Web Apps. To set up the workflow, you can either:

* Remove the __.template__ extension from the __.github/workflows/azure-static-web-apps.ymltemplate__ file, replace the secrets in the file with your own values, and commit the changes to the__main__ branch. The workflow will then be triggered automatically.
* Use an existing workflow file. To build an Angular Universal application, specify the custom build command and the output directory in the workflow file:

```yaml
  - name: Build And Deploy
    id: builddeploy
    uses: Azure/static-web-apps-deploy@v1
    with:
      azure_static_web_apps_api_token: ${{ secrets.YOUR_API_TOKEN }} # Replace with the name ofyour secret
      repo_token: ${{ secrets.GITHUB_TOKEN }}
      action: "upload"
      app_location: "/"
      output_location: "dist/angular-universal-swa-basic/browser" # Change this; uses the output location of the Angular Universal application
      app_build_command: "npm run prerender -- --routes-file routes.txt" # Add this; uses theprerender command to build the Angular Universal application
```
