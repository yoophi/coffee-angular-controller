Angular with CoffeeScript
=========================

coffeescript 를 이용하여 angularjs 어플리케이션을 작성할 때, 
사용할 수 있는 BaseController 와 BaseService 입니다.

## 설치 

```
$ bower install yoophi/coffee-angular-controller
```

## 사용

```
class AppController extends BaseController
  @inject '$scope'
  
  initialize: () ->
    @$scope.foo = 'bar'
    
  sayHello: (name) ->
    @$scope.hello = "Helli, #{name}"
    
    
angular.module 'app'
.controller 'AppController', AppController
```

## Build

```
$ gulp coffee
```