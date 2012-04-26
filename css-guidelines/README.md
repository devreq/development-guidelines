CSS Guidelines
==============

* Put CSS in the document head.

* Avoid the universal key selector.

* Make your rules are as specific as possible by using class selectors over 
  tag selectors.

* Avoid using descendant selectors, especially those that specify redundant 
  ancestors.

  ```css
  body ul li a { ... }
  ```

* Do not work with `!important`. Not only because IE =< 7 can't deal with it. 
  In a complex structure, the use of `!important` is often tempting to change 
  a behavior whose source can't be found, but it's *poison* for long-term 
  maintenance.

* Avoid CSS expressions. They considerably degrade rendering performance are 
  not supported as of IE8.


References
----------

* [Optimize browser rendering - Make the Web Faster - Google Developers][r1]

[r1]: https://developers.google.com/speed/docs/best-practices/rendering
