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


Documentation
-------------

For documentation living outside of the code, we use simple text files written 
in [Markdown][md]. Since all of these documents are published on GitHub we 
can use the extra features provided by their Markdown parser; [Redcarpet][rc].


[md]: (http://daringfireball.net/projects/markdown/syntax)
[rc]: https://github.com/tanoku/redcarpet