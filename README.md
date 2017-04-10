## Website Performance Optimization portfolio project

## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>




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
