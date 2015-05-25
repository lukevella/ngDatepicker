# ngDatepicker

An AngularJS datepicker directive created for use in [Rallly](http://github.com/lukevella/Rallly).

[View Demo](http://lukevella.github.io/ngDatepicker/)

## Dependencies

You will need:

* AngularJS (1.x)
* [date.js](http://www.datejs.com) (included)

## Install

To use you will need to add the following scripts after you include AngularJS

``` html
<!-- AngularJS -->
<script src="path/to/js/date.js"></script>
<script src="path/to/js/ng-datepicker.js"></script>
```

Add the stylesheet

``` html
<link rel="stylesheet" href="path/to/css/ng-datepicker.css">
```

## How to use

Add the `ngDatepicker` module as a dependency to your app.

``` javascript
var app = angular.module('myApp',['ngDatepicker'])
```

Then just add the `datepicker` attribute to an element along with an `ng-model`. Optionally, you can choose to pass a `control` attribute which will allow you to remove dates from the date picker programmatically.

``` html
<body ng-app="myApp">
    <div datepicker ng-model="myModel" control="myControl">

    </div>
    <ul>
        <li ng-repeat="date in myModel">
            {{date}} 
            <button ng-click="myControl.removeDate(date)">Remove</button>
        </li>
    </ul>
</body>
```

