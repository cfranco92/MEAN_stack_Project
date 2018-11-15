# MEAN_stack_Project
Project developed using full stack JavaScript.
MEAN = MongoDB, Express, Angular y Node.js

## 1. Technical specifications
Remember that a stack is a set of technologies, possible combinations to complete a project. 
MEAN is a one of the most important stack and with the largest community in the software industry today.

## 2. What is MEAN?
A development stack is like your toolbox. It is the set of technologies that we use to develop a project, be it a web application, an application for mobile devices or what you want create.

To build a web application, for example, we can use Backbone or React for out frontend and Node, PHP or Rails for the backend. We can run our code inside a virtual machine like Vagrant or develop directly in our computer there are many options and you can combine them as you want, of course, some combinations represent better performance in your applications, there are well known and well tested combinations that have good behavior as MEAN.

MEAN is one of the most used technology stacks to create Single Page Applications:
* MongoDB for the database
* Express as a frameworkbackend running on Node.js
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

## 4. Installation and configuration of the environment configuration
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