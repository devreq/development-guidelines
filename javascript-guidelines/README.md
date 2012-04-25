JavaScript Guidelines
=====================

* Use camel case for variables and functions, uppercase 
  for constants and pascal case for constructors.

  ``` javascript
  
  // Variables in camel case
  var ourCompanyName = "Hemnet";
  
  // Functions in camel case
  function getCompanyName() {
      return ourCompanyName;
  }
  
  // Constants in uppercase
  var URL = "http://hemnet.se/";
  
  // Constructors in pascal case
  function Person(name) {
      this.name = name;
  }
  ```

* Use `===` and `!==` instead of `==` and `!=` to vaoid type coercion errors.

* All variables and functions should be declared before they are used

* Variable declarations should take place at the beginning of a function using 
  a single `var` statement with one variable per line.

* When a function is not a method (not attached to an object) it should be 
  defined using function declaration format (not function expression format 
  nor using the `Function` constructor).

  ```
  // Good
  function doSomething(arg1, arg2) {
      return arg1 + arg2;
  }

  // Bad: Function expression
  var doSomething = function(arg1, arg2) {
      return arg1 + arg2;
  }
  ```

* Strict mode should be used only inside of functions and never globally.

* Never use `eval()`.

* Never use the `with` statement. This statement isn't available in strict mode 
  and likely won't be available in future ECMAScript editions.

* Don't prevent action with `return false`. Instead use `preventDefault()` and 
  `stopPropagation()`, since they don't stop further code from being triggered.


References
----------

* [Maintainable JavaScript][r1]
* [jQuery Events: Stop (Mis)Using Return False][r2]

[r1]: http://www.amazon.com/Maintainable-JavaScript-Nicholas-C-Zakas/dp/1449327680?tag=nczonline-20
[r2]: http://fuelyourcoding.com/jquery-events-stop-misusing-return-false/
