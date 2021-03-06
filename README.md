Angular-complexify v0.3.1 [![Build Status](https://travis-ci.org/Kraku/angular-complexify.svg?branch=master)](https://travis-ci.org/Kraku/angular-complexify)
===============
#### password strength validation
AngularJS port of [jquery.complexify.js](https://github.com/danpalmer/jquery.complexify.js)

## Installing
```js
var myApp = angular.module('myApp', [
  'angular-complexify'
]);
```

## Usage
In javascript (provider)
```js
myApp.controller('SomeCtrl', ['$scope', 'Complexify', function($scope, Complexify) {
  $scope.test = Complexify('somePassword');
}]);
```

In template (directive)
```html
<input type="text" ng-model="password">

<p ng-show="password">
 <span complexify="password"></span>%,
 <span complexify="password" type="verbal"></span>
</p>
```

In template (filter using ui-bootstrap progressbar)
```html
<progressbar value="password | complexify"></progressbar>
```

## Tests
```
npm install
grunt karma:unit
```
<br>
---
© 2014 [Maciej Podsiedlak](http://mpodsiedlak.com) (WTFPL v2 licence)
