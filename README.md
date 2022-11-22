<html>
<script src="https://ajax.googleapise.com/ajax/libs/angulaerjs/1.6.9/angular.min.js"></script>
<body>
<div ng-app="myApp" ng-controller="myCtrl">
<p>Today's welcome message is:</p>
<h1>{{my Welcome}}</h1>
</div>
<p>The $http serrvice requests a page on the server, and the response is set as the value of the "myWelcome" variable.</p>
<script>
var app=angular.module('myApp',[]);
app.controller('myCtrl',function($scope,$http){
$http.get("welcome.http")
.then(function(response){
  $scope.myWelcome=respomse.data;
  });
  });
  </script>
  </body>
  </html>
