## Website Performance Optimization portfolio project

#### Part 1: Optimize PageSpeed Insights score for index.html

------------------------------------------------------------

Profiling
-----------------------------------------------------------

Used Google PageSpeed Insights at https://developers.google.com/speed/pagespeed/ and checked the speed of the desktop and mobile version.

Images
----------

Optimizing:
Google PageSpeed suggests to optimize the images:

Named pizzeria.jpg to pizzeria2.jpg.
Optimized the size of the image to 4,05 kB and shrunk pizzeira.jpg to
width - 100 pixels
Height - 75 pixels

Javascript
------------

Optimizing:
Added async to the scripts and moved the js perfmatters and google analytics script to the bottom of the page.

CSS
-------------

Optimizing:
Remove Google Web font.
Place CSS inline and minified on index.html.
Added a media query media="print".

Result - Final Mesuring:
-----------------------

The Google PageSpeed Insight Score for the mobile version of index.html changed to 94/100 and desktop version to 95/100. Hosted the site on github as github pages. Unable to include cache to the browser due to github restrictions.

#### Part 2: Optimize Frames per Second in pizza.html

------------------------------------------------------------
Javascript
------------

- Replaced "querySelector" with "getElementById", since the selectors are not too complex.
- Replaced "querySelectorAll" with "getElementsByClassName".
- Created a new variable allPizzaContainers for all pizza containers to apply dx and newwidth to all pizza containers; Placed all variables out of the for loop.
- Placed the variable pizzasDiv in the for loop outside the for loop.
- Added createDocumentFragment to create a imaginary node to append its values to the pizza.html.

CSS
-------------

- Added transform to force hardware acceleration
transform: translateZ(0);
will-change: transform;


Final Mesuring
-------------

- Time to generate pizzas on load: 49.92ms
- Average scripting time to generate last 10 frames: 0.39899999999997815ms (best time recorded)
