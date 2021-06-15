# Angular_Tutorial

Here are the key notes I jotted down while reading about Angular

## What is Angular?

Angular is a platform and framework for building single-page client applications using HTML and TypeScript. Angular is written in TypeScript.

The basic building blocks of the Angular framework are Angular components that are organized into NgModules.

NgModules collect related code into functional sets; an Angular application is defined by a set of NgModules

- **Components define *views***, which are sets of screen elements that Angular can choose among and modify according to your program logic and data.
- **Components use *services***, which provide specific functionality not directly related to views. Service providers can be *injected* into components as *dependencies*, making your code modular, reusable, and efficient.

Modules, components and services are classes that use decorators. These decorators mark their type and provide metadata that tells Angular how to use them

Metadata for a component class associates it with a template that defines a view. 

A template combines ordinary HTML with Angular directives and binding markup that allow Angular to modify the HTML before rendering it for display.

Metadata for a service class provides the information Angular needs to make it available to components through dependency injection (DI).

Angular provides the Router service to help you define navigation paths among views. The router provides sophisticated in-browser navigational capabilities.

## Modules:

An NgModule declares a compilation context for a set of components that is dedicated to an application domain, a workflow, or a closely related set of capabilities

NgModule can associate its components with related code, such as services, to form functional units

root module, conventionally named AppModule, which provides the bootstrap mechanism that launches the application

Organizing your code into distinct functional modules helps in managing development of complex applications, and in designing for reusability, lets you take advantage of lazy-loading

lazy-loading—that is, loading modules on demand—to minimize the amount of code that needs to be loaded at startup.

## Components:

Root component that connects a component hierarchy with the page document object model (DOM).

Each component defines a class that contains application data and logic, and is associated with an HTML template that defines a view to be displayed in a target environment.

@Component() decorator identifies the class immediately below it as a component, and provides the template and related component-specific metadata.

## Templates,Directives, Data binding:

A template combines HTML with Angular markup that can modify HTML elements before they are displayed

Template directives provide program logic, and binding markup connects your application data and the DOM.

### Data Binding:

1. **Event Binding**: lets your application respond to user input in the target environment by updating your application data.
2. **Property Binding**: lets you interpolate values that are computed from your application data into the HTML.

Before a view is displayed, Angular evaluates the directives and resolves the binding syntax in the template to modify the HTML elements and the DOM, according to your program data and logic.

Supports two-way data binding, meaning that changes in the DOM, such as user choices, are also reflected in your program data.

Templates can use **pipes** to improve the user experience by transforming values for display.

Ex: use pipes to display dates and currency values that are appropriate for a user's locale

## Services and Dependency Injection

For data or logic that isn't associated with a specific view, and that you want to share across components, you create a service class

A service class definition is immediately preceded by the @Injectable() decorator. 

The decorator provides the metadata that allows other providers to be injected as dependencies into your class.

Dependency injection (DI) lets you keep your component classes lean and efficient. 

They don't fetch data from the server, validate user input, or log directly to the console; they delegate such tasks to services.

### Routing:

[Router](https://angular.io/api/router/Router) NgModule provides a service that lets you define a navigation path

- Enter a URL in the address bar and the browser navigates to a corresponding page.
- Click links on the page and the browser navigates to a new page.
- Click the browser's back and forward buttons and the browser navigates backward and forward through the history of pages you've seen.

The router maps URL-like paths to views instead of pages

User performs an action, such as clicking a link, that would load a new page in the browser, the router intercepts the browser's behavior, and shows or hides view hierarchies.

The router interprets a link URL according to your application's view navigation rules and data state

You can navigate to new views when the user clicks a button or selects from a drop box, or in response to some other stimulus from any source

The router logs activity in the browser's history, so the back and forward buttons work as well.

To define navigation rules, you associate navigation paths with your components. 

A path uses a URL-like syntax that integrates your program data, in much the same way that template syntax integrates your views with your program data. 

You can then apply program logic to choose which views to show or to hide, in response to user input and your own access rules.


Source: https://angular.io/guide/architecture
