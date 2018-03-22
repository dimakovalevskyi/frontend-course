# AngularJS basics

## AngularJS application structure

Application == module

```
// create module 'myModule'
angular.module('myModule', []);


<html ng-app="myModule">
```

### run

```
// create run block in 'myModule' module
angular.module('myModule')
    .run(function() {
        alert('It works!');     
    });

```

```
// create run block in 'myModule' module
angular.module('myModule')
    .run(function() {
        alert('First!');     
    })
    .run(function() {
        alert('Second!');     
    });

angular.module('myModule')
    .run(function() {
        alert('And one more!');     
    });
```

### config

```
// create config block in 'myModule' module
angular.module('myModule')
    .config(function() {
        alert('I will be before all run blocks!!!');     
    });

```

### constant and value

```
angular.module('myModule')
    .constant('MY_FIRST_CONSTANT', 666)
    .constant('ONE_MORE_CONSTANT', 'Hello!')
    .constant('MY_FIRST_OBJECT_CONSTANT', {
            property1: 1,
            property2: 'I love angularJS!'
        })
    .value('valueNumberOne', 1);

angular.module('myModule')
    .value('valueNumberTwo', 2);    
```

### Dependency Injection

```
angular.module('myModule', [])
    .run(['depService', 'depService2', function(depService, depService) {
      // ...
    }])
    .config(['depProvider', function(depProvider) {
      // ...
    }])
    .directive('directiveName', [function() {
      // ...
    }]);
```

### controller

```
angular.module('demo').controller('mainController', ['$scope', function($scope) {
    $scope.heading = 'Hello, world!';
    $scope.heading2 = 'My first angularJS application works!!!!!';
}]);


<div class="container" ng-controller="mainController">
    <h1>{ { heading } }</h1>
    <hr>
    <h2>{ { heading2 } }</h2>
</div>
```

### directive, service, provider, factory, decorator, filter, animation, component

## AngularJS application cifecycle

 * Angular framework defining
 * Register all modules with all services and blocks
 * Create all providers
 * Run all config blocks
 * Create all services/factories/value/...
 * Run all run blocks
 * Create all directives
 * Render html code and apply all controllers/directives/components/...
 
## Basic AngularJS directives

 * `ng-bind`
 * `ng-model`
 * `ng-repeat`
 * `ng-init`
 * `ng-show`
 * `ng-hide`
 * `ng-if`
 * `ng-class`

## Example 

 Buttons generator

## Useful [link](https://habrahabr.ru/post/190342/)
