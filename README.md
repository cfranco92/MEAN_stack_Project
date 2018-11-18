# MEAN_stack_Project
Project developed using full stack JavaScript.
MEAN = MongoDB, Express, Angular y Node.js

## 1. Technical specifications
Remember that a stack is a set of technologies, possible combinations to complete a project. 
MEAN is a one of the most important stack and with the largest community in the software industry today.

---
## 2. What is MEAN?
A development stack is like your toolbox. It is the set of technologies that we use to develop a project, be it a web application, an application for mobile devices or what you want create.

To build a web application, for example, we can use Backbone or React for out frontend and Node, PHP or Rails for the backend. We can run our code inside a virtual machine like Vagrant or develop directly in our computer there are many options and you can combine them as you want, of course, some combinations represent better performance in your applications, there are well known and well tested combinations that have good behavior as MEAN.

MEAN is one of the most used technology stacks to create Single Page Applications:
* MongoDB for the database
* Express as a framework backend running on Node.js
* And Angular for the frontend

These technologies are very simple to combine: everything is written in JavaScript, even the database saves collections with objects in JSON.

Node.js is our web server, in charge of listening to users requests and responding with the data they require.
* Configure your routes
* Protect resources
* Serve static files

Express is the micro-framework that will make our lives much easier, allowing us to save time and line of code. At the same time it gives us the freedom to organize the files and use the modules we need for our project.

At this point it is important that we talk about data persistence. MongoDB is one of the NoSQL databases most used today. It allows us to store objects in JSON format without a rigid data schema, as in relational data.
From Express we will ask for data to the database, who will respond to our queries.

But all this does not make sense it the users can not acces our application visually: Angular is the tool of our box that completes de stack. It is one of the most popular frameworks, tih one of the largest and most active communities in frontend development.

With Angular we can create visual and reusable components throughout our project or even in other projects. Develop injectable services in these components to communicate with the backend making requests for data and receiving the answers.

![MEAN process](/images/server.png)

---
## 3. Introduction to Angular and TypeScript
### Angular
* Is a framework for Frontend.
* Has option actually to run frome Backend y can re-use the code.
* It allows us to organize the files that we are going to have and to separate the responsibilities of each file. It allows us to separate our application into reusable components.
* This framework, of what is going to be treated more is about components. The componenents are visual units reusable and with cretain defined behavior.
* Another thing that Angular is going to solve is routing, that is, the routing system.
* Angular will also give us the services. Are ways to connect with the Backend, from there we will ask for certain data that the Frontend need to display on the screen.
* Angular offers a system of template. Each component will have associated a template or view that will be the HTML structure that it has.
* From Angular it is possible that we can define our own labels to define the reusable components.
* Another thing that Angular allows us are the modules. They are complete libraries with components and directives already armed or pre-established. An example is Angular Material that is what we will be using for our project.
* CLI = Command Line Interface or Command Line Interface.
* Google is behind Angular. It's the Google developer who support this Open Source library.
* Angular is very adapted and has a very large community around.

### TypeScript
* It's a super set of JavaScript. It will help us to expand JavaScript capabilities a bit, it will incorporate a type check to correct errors. It will incorporate a type check to correct errors.
* It is an ideal technology for work in team projects.

### Angular Developer Experience
One of the points in favor is that every time we make changes in our files they will be reflected in our browser automatically without having to recompile by hand and without having to refresh.

---
## 4. Installation and configuration of the Angular environment
We need to define our editor, in our case we will use VS-Code.

Another tools we will use is the console or terminal. In our case we will use Hyper or Iterm2 on MacOS.

Another tool we will use is the Angular CLI, with commands to management Angular environment.

We need to install the newest version of Node that we can find on the [official website of Node community](https://nodejs.org/en/).

Also we need to install Angular console and other features of Angular from the [official website of Angular](https://cli.angular.io/).
```terminal
    $ npm install -g @angular/cli
```

We can get more information about Angular in NPM web in the [section of Angular/CLI in NPM](https://www.npmjs.com/package/@angular/cli).

Now we can create a new project of Angular with the next command:
```
    $ ng new [projectName]
```

Then we can run project with local server with the next command:
```terminal
    $ ng serve
```

---
## 5. Working with Angular Material

Important data:
* Angular Material are components based on Material Design for Angular.
* package.json is like the manifesto of our projects, is where all the details are.

Now we need to incorporate Material Design following [this manual](https://material.angular.io/guide/getting-started) through the Angular Material website.

### Steps 
1. Install Angular Material, Angular CDK and Angular animations

    We need to install it in the following way:
    ```
        $ npm install --save @angular/material @angular/cdk @angular/animations
    ```
    <br>
2. Configure Animations

    Once the animations package is installed, import BrowserAnimationsModule into your application to enable animations support.

    ```TypeScript
        import {BrowserAnimationsModule} from   '@angular/platform-browser/animations';

        @NgModule({
            ...
            imports: [BrowserAnimationsModule],
            ...
        })
        export class PizzaPartyAppModule { }
    ```
    <br>
    Alternatively, you can disable animations by importing NoopAnimationsModule.

    ```TypeScript
        import {NoopAnimationsModule} from '@angular/platform-browser/animations';

        @NgModule({
            ...
            imports: [NoopAnimationsModule],
            ...
        })
        export class PizzaPartyAppModule { }
    ```
    <br>

3. Import de components modules

    Import the NgModule for each component you want to use:
    ```TypeScript
        import {MatButtonModule, MatCheckboxModule} from '@angular/material';

        @NgModule({
            ...
                imports: [MatButtonModule, MatCheckboxModule],
            ...
        })
        export class PizzaPartyAppModule { }
    ```
    <br>

    Alternatively, you can create a separate NgModule that imports all of the Angular Material components that you will use in your application. You can then include this module wherever you'd like to use the components.
    ```TypeScript
        import {MatButtonModule, MatCheckboxModule} from '@angular/material';

        @NgModule({
            imports: [MatButtonModule, MatCheckboxModule],
            exports: [MatButtonModule, MatCheckboxModule],
        })
        export class MyOwnCustomMaterialModule { }
    ```
    <br>

4. Include a theme

    Including a theme is required to apply all of the core an theme styles to your application.
    <br>
    To get started with a prebuilt theme, include one of Angular Material's prebuilt themes globally in your application. if you're using the Angular CLI, you can add this to your style.css:
    ```css
        `@import "~@angular/material/prebuilt-themes/indigo-pink.css";
    ```
    <br>
    If you are not using the Angular CLI, you can include a prebuilt theme via a ```<link>``` element in your ```index.html```.

    For more information on theming and instructions on how to create a custom theme, see the [theming guide developed by Google](https://material.angular.io/guide/theming).
    <br>

5. Gesture Support

    We gonna install hammerjs as another NodeJS resource.
    Some components (```mat-slide-toggle```,```mat-slider```,```matTooltip```) rely on HammerJS for gestures. In order to get the full feature-set of these componenents, [HammerJS](http://hammerjs.github.io/) must be loaded into the application.
    <br>
    You can add HammerJS to you application via [npm](https://www.npmjs.com/package/hammerjs), a CDN (such s the [Google CDN](https://developers.google.com/speed/libraries/#hammerjs)), or served directlye from your app.
    <br>
    To install via npm, use the following command:
    ```TypeScript
        $ npm install --save hamerjs
    ```
    <br>

    After installing, import it on your app's root module.
    ```JavaScript
        import 'hammerjs'
    ```
    <br>

6. Add material icons

    If you want to use the md-icon component with the official [Material Design Icons](https://material.io/tools/icons/?style=baseline), load the icon font in your ```index.html```.
    ```html
        <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    ```
    <br>
    The other fonts that we will use in this project are:

    ```
        https://fonts.google.com/?query=roboto&selection.family=Roboto
    ```

---
## 6. Construction header of the application
In this section we will configure the toolbar for our application.

Now we are going to include mat-toolbar in the ```material.module.ts``` file.

```TypeScript
    import {MatToolbarModule} from '@angular/material';
    
    const modules = [
        MatToolbarModule,
        MatIconModule
    ];
```
<br>

Then, in ```app.component.html``` file, we will include the following example:
```html
    <mat-toolbar color="primary">
        <mat-toolbar-row>
            <span>Custom Toolbar</span>
        </mat-toolbar-row>

        <mat-toolbar-row>
            <span>Second Line</span>
            <span class="example-spacer"></span>
            <mat-icon class="example-icon">verified_user</mat-icon>
        </mat-toolbar-row>

        <mat-toolbar-row>
            <span>Third Line</span>
            <span class="example-spacer"></span>
            <mat-icon class="example-icon">favorite</mat-icon>
            <mat-icon class="example-icon">delete</mat-icon>
        </mat-toolbar-row>
    </mat-toolbar>
```
<br>

Then, we should search one icon in this link, to add to the toolbar.
```url
    https://material.io/tools/icons
```
<br>

Then, in material.module.ts we need to add this code:
```TypeScript
    import { MatIconModule} from '@angular/material';

    const modules = [        
        MatIconModule
    ];

    @NgModule({
        imports: [modules],
        exports: [modules],
    })
```
<br>

Now, we need to add style in ```styles.css``` to our toolbar and add spaces between words in ```app.component.css```.
```css
    .space {
        flex: 1 1 auto;
    }
```
<br>
```css
    body {
        margin: 0;
        font-family: 'Roboto';
    }
```
<br>