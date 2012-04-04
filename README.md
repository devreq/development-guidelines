Development Guidelines
======================

The following documents are guides to assist in the production, implementation 
and continuing development of Hemnet.se and accompanying products. To ensure 
design continuity and maintain the life span of these products, it is 
important that everybody involved read, understand and adhere to these rules.


Contributing
------------

These guidelines are living documents and feedback is accepted in the form of 
pull requests which promotes discussions and ensures that changes are reviewed 
and accepted by all team members before being going live.

Changes are not to be merged before all team members that the changes concern 
make a comment in the pull request which says “OK” or something to that effect.


Coding Conventions
------------------

Shared coding guidelines that provides consistency and maintainability by 
offering the same set up regardless of current environment and code base.

* Use soft-tabs with a two space indent.

* Aim to keep lines fewer than 80 characters.

* Never leave trailing whitespace.

* Use spaces around operators, after commas, colons and semicolons, around `{` 
  and before `}`.

* No spaces after `(`, `[` or before `]`, `)`.

### Code Examples

~~~~ html
<div itemscope itemtype="http://schema.org/Product">
  <h3 itemprop="name">Fågelsundet 257, Fågelsundet, Vid havet, Tierp</h3>
~~~~

~~~~ css
#product {
  width: 320px;
  background: #FFC url(/images/product_bg.png) no-repeat;
}
~~~~

~~~~ javascript
var add = function(a, b) {
  return a + b;
}
~~~~

~~~~ ruby
sum = 1 + 2
a, b = 1, 2
1 > 2 ? true : false; puts 'Hi'
[1, 2, 3].each { |e| puts e }
~~~~


Documentation
-------------

For documentation living outside of the code, we use simple text files written 
in [Markdown][md]. Since all of these documents are published on GitHub we 
can use the extra features provided by their Markdown parser; [Redcarpet][rc].


[md]: (http://daringfireball.net/projects/markdown/syntax)
[rc]: https://github.com/tanoku/redcarpet