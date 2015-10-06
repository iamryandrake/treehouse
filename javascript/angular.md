# AngularJS

<a href="http://referrals.trhou.se/rdrakey" target="_blank">
<img src="https://static.teamtreehouse.com/assets/content/referral-badge-grn.png" style="width:30%;height:30%;"/>
</a>

@mrvdot
What is an MVC?

Two primary types that are commonly used.
Two Common Types of JavaScript Libraries
- DOM Manipulation Libraries
- MVC Frameworks

A DOM Manipulation library's first focus is on the HTML view. This means that the library does its work on the existing html and css that the browser has already rendered. In comparison, MVC Frameworks start with the data first and build the view from that data.

MVC (Model, View, Controller):
Model: The data we care about
View: What the user sees
Controller: Contains all the necessary logic to connect the model with the view

Why Use an MVC Framework?

Use Case where most valuable: primary reason should be your data. Anytime your data is dynamic, an MVC is often the right choice.

MVC connects the view and the data we store (model), allowing users to update the data.

The next question we want to ask is “when should you use an MVC framework”, accompanied by it’s corollary, "when *shouldn’t* you use one, or when is something else more appropriate?"

An MVC Framework is phenomenal at:
- Handling your data
- Listening to specific user interactions
- Presenting data (or changes) back to the user
- Providing a pipeline between your data and the views that the user sees, as well as the various input points that allow the user to interact with and/or change that data

Ask yourself: Am I trying to improve the visualisation of the data that's already there or actually connect to new properties or combinations of properties?

ng-model
Why Angular?

Angular follows a very intentional pattern of being data-driven. Everything is declarative from the beginning. When you're writing your HTML, each element or collection of elements gets to declare what properties they are bound to. Some of these, by nature, will be read-only. Some will both read and write to that property. Again, we declare those details by the elements we choose and the attributes we give them. Any time the value for a property changes, all those elements that have declared those bindings will respond accordingly.

$scope - Serves as the connection between the model(our data) and the views(what the user sees)

Four main elements of Angular:
- Directives: The fundamental building block of Angular. They serve as the definitions for various declarations you want to use within your Angular application. They form the connection between the attribute you associate with a DOM element and the JavaScript code that turns that attribute into actual functionality. Directives are intended to be small modules that can be dropped in and just work, or combined with other directives.
- Factories: Used to maintain one single instance of something. They are often used for maintaining state. Additionally, they can be used to provide an abstraction layer between your directives and your APIs.
- Controllers: Have a lot of similar functionality to directives, but they are predominently used just for data connections and logical restraints around them. Unlike a directive, they cannot contain any extra templating or complex ordering.
- Filters: Used to implement temporary transformations of data as it travels between the model and the view.

Introduction to Two-Way Data Binding
Two-way data binding is integral to what makes Angular.JS so powerful. Instead of trying to remember to update each representation of your data everytime there’s a change, with data binding it all happens automatically.

For "read" access, instead of 'ng-model' you can use: {{property}}.


Services and Dependencies

What is dependency injection?
In short, it means each component is responsible for declaring its own dependencies.

Services: helper libraries that provide some additional functionalities.

$http: A service for making AJAX calls and handling their responses.

Services are singletons, and thus once initialized, the same instance is sent to every component that depends on it.

angular.module('httpTest', [])
  .factory('People', function () {
    var people = [];

    })
  .controller('appCtrl', function ($scope, $http) {
    $scope.people = [];

    $http.get('people.json')
      .success(function (response) {
        $scope.people = response;
      })
      .error(function (err) {
        alert(err);        
      });

      $scope.save = function (person) {
        $http.post('people.json', person)
          .success(function (response) {
            alert('Person saved successfully');
            })
          .error(function (err) {
            alert('Unsuccessfully saved person');
          });
    });

    Controllers and directives are largely stateless.

    What is a directive?

They are building block of any Angular application. They can be collection of functionality packaged up that can be dropped anywhere within your app. Two basic ingredients: The attribute or set of attributes that we use to declare an HTML node and 2. the JavaScript that implements that functionality.

How to label directives:
- Within HTML, use dashes, like this: contact-card
- Within JavaScript, use camelCase, like this: contactCard.

Restrict properties

E = element
A = attribute
C = Classname
M = Comment

How to insert a directive into the DOM:
1. By adding an Attribute to an element, like this:
<div contact-card="person"></div>
2. By creating a new Element:
<contact-card></contact-card>
3. RARE: By giving an element a classname, like this:
<div class="contact-card"></div>
4. RARE: By using an HTML comment, like this:
<--!contact-card-->


$rootScope
The top level data object that will manage the lifecycle of our web app

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain

Look up isolateScope

If you use more than one directive on the same element, they share the scope. Most restricted scope wins (isolateScope), and can't have two isolateScopes as Angular doesn't know how to merge the two together.

ng-model: the most common directive, and the key to two-way data binding. The directive should always have a 'dot', meaning it's accessing a property nested inside an object, such as:
ng-model="person.name"

ng-click: allows us to fire actions in response to the user clicking on an element

ng-show/ng-hide: allows you to easily show or hide an element based on a conditional expression. Usually for if statements, but properties are against $scope.
ng-show="person.email"
ng-hide="!person.email"

ng-repeat: this directive lets you iterate over a collection and display one or more elements for each instance

$attrs.$observe

$parsers $(views to model)

$formatters (model to view)

$apply

$setValidity
