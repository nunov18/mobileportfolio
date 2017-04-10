## Website Performance Optimization portfolio project

#### Part 1: Optimize PageSpeed Insights score for index.html

------------------------------------------------------------

Profiling - Optimizing - Measure - Lather - Rinse - Repeat
-----------------------------------------------------------
Profiling:
Used Google PageSpeed Insights at https://developers.google.com/speed/pagespeed/ and checked the speed of the desktop and mobile version.

Measuring:
Score for mobile version was 28/100 and for desktop version 30/100.


Images
----------
Optimizing:
Google PageSpeed suggests to optimize the images:

pizzeria.jpg
Optimized the size of the image to 2,79 kB and shrunk pizzeira.jpg to 115 pixels wide, down from 2048 pixles wide.

Javascript
------------

Optimizing:
I added async to the scripts and moved the js perfmatters and google analytics script to the bottom of the page.

CSS
-------------

Optimizing:
Remove Google Web font.
Place CSS inline on index.html.
Added a media query <link href="css/print.css" rel="stylesheet" media="print">

Hosting & Browser Cache
-----------------------
Since I host the site on github as github pages, it is not possible to include cache to the browser.  

Result:
The Google PageSpeed Insight Score for the mobile version of index.html changed to 94/100 and desktop version to 95/100.

#### Part 2: Optimize Frames per Second in pizza.html
