#Web Optimization Project


## Better performance for index.html
-------------

**Please note: You´ll find the original html-file under the name index_src.html. The index.html contains minified production code**

###Where I modified the code:

1. Giving google-analytics the attribute "async" to stop the script blocking the rendering

2. Inlinening the css (style.css) into style-tags in the head to reduce the critical rendering path.

3. Giving the css (print.css) the proper media-attribute (media=print).

4. Optimized the two pictures, which are not downloaded from other sources.

5. Loading google fonts asynchronously with Web Font Loader (source: https://github.com/typekit/webfontloader).

6. Bringing the javascript (google analytics and perfmatter.js to the end of the file to avoid render blocking effects)



## Better performance for pizza.html

1. Fixing the pizza-slider: Changing the function changePizzaSizes. Built in a switch-statement before the loop. Deleting the call of the complex function determineDx. Putting the DOM-queries in a variable outside the foreloop.

2. Changing the variable var items into document.getElementsByClassName('.mover');

3. In document.addEventListener('DOMContentLoaded', function()... we reduce the number of pizzas created to 32.

4. function updatePositions: declaring a new var for not always have to go through the DOM.
