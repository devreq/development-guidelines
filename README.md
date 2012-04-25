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

* Double quotes (`"`) are preferred to single quotes (`'`), expect for strings 
  containing double quotes.

* Use soft-tabs with a two space indent.

* Aim to keep lines fewer than 80 characters.

* Line breaking is typically done after an operator and the next line is 
  indented two levels.

* Never leave trailing whitespace.

* Blank lines should be used to separate lines of code from unrelated lines of code.

* Use spaces around operators, after commas, colons and semicolons, around `{` 
  and before `}`.

* No spaces after `(`, `[` or before `]`, `)`.

### Code Examples

```html
<div itemscope itemtype="http://schema.org/Product">
  <h3 itemprop="name">Fågelsundet 257, Fågelsundet, Vid havet, Tierp</h3>
</div>
```

```css
#product {
  width: 320px;
  background: #FFC url(/images/product_bg.png) no-repeat;
}
```

```javascript
var add = function(a, b) {
  return a + b;
}
```

```ruby
sum = 1 + 2
a, b = 1, 2
1 > 2 ? true : false; puts "Hi"
[1, 2, 3].each { |e| puts e }
```


Commenting
----------

Make frequent use of comments to aid others in understanding your code. Use comments when:

* Code is difficult to understand.

* The code might be mistaken for an error.

* Browser-specific code is necessary but not obvious.

* Documentation generation is necessary for an object, method, 
  or property (use appropriate documentation comments).


### Comment annotations

Comments may be used to annotate pieces of code with additional information. These 
annotations take the form of a single word followed by a colon. The acceptable 
annotations are:

* `TODO` – indicates that the code is not yet complete. Information about the next 
           steps should be included.

* `HACK` – indicates that the code is using a shortcut. Information about why the 
           hack is being used should be included. This may also indicate that it 
           would be nice to come up with a better way to solve the problem.

* `XXX` – indicates that the code is problematic and should be fixed as soon as possible.

* `FIXME` – indicates that the code is problematic and should be fixed soon. Less 
            important than `XXX`.

* `REVIEW` – indicates that the code needs to be reviewed for potential changes.


Documentation
-------------

For documentation living outside of the code, we use simple text files written 
in [Markdown][md]. Since all of these documents are published on GitHub we 
can use the extra features provided by their Markdown parser; [Redcarpet][rc].


Credits
-------

Other open manuals, articles, guidelines, style guides, etc. that has 
inspired and helped us to put these development guidelines together.

* [What is good code?](http://robots.thoughtbot.com/post/21781129461/what-is-good-code)
* [GitHub Styleguide](https://github.com/styleguide)


[md]: http://daringfireball.net/projects/markdown/syntax
[rc]: https://github.com/tanoku/redcarpet