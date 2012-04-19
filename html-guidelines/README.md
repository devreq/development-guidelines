HTML Guidelines
===============

* Use lowercase for all elements and attribute names.

* Explicitly include all start and end tags.

*   Quote all attribute values and do not use any whitespace around the equals sign.

    ``` html
    <header role="banner"></header>
    ```

*   Only use <a> for actual working links.

    If you can't deliever a page on mouse click, it's not a hyperlink.

    ``` html
    <!-- Breaking the web by introducing accessibility and usability problems. --> 
    <a href="#"></a>

    <!-- How it should be done. -->
    <span role="link"></span>
    ```

*   Always use `alt` text on `img`'s. Without it, they're unaccessible.

    ``` html
    <!-- Valid and descriptive example. -->
    <img alt="Marvin in the spaceship cabin" src="marvin.png">
    
    <!-- Valid example for a decorational image without meaning. -->
    <img alt="" src="decoration.png">
    
    <!-- Inaccessible and not to be used - ever. -->
    <img src="silver_dog.jpg">
    ```

* Tabular data in tables and never for layout, with one exception: HTML emails.

References
----------

* [HTML5 syntax guidelines – 456 Berea Street][r1]
* [End tags, semi-colons and maintainable code – 456 Berea Street][r2]
* [Let's talk about semantics][r3]

[r1]: http://www.456bereastreet.com/archive/201011/html5_syntax_guidelines/
[r2]: http://www.456bereastreet.com/archive/201204/end_tags_semi-colons_and_maintainable_code/
[r3]: http://html5doctor.com/lets-talk-about-semantics/
