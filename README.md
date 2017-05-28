## Website Performance Optimization portfolio project
# Website Optimization Project

Welcome to my website optimization project.  Please see below for details regarding
how to access the page and details of the optimizations performed.

### Getting started

The site is hosted on the github pages platform.  The pages can be accessed at
https://bjm2020.github.io/frontend-nanodegree-mobile-portfolio/ or downloaded from github
and hosted on your own server.

I reccommend python's simple http server.  

'''bash
$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080

'''

Open a browser and visit localhost:8080


#### Part 1: Optimize PageSpeed Insights score for index.html

The following optimizations were perfomed on the index.html portfolio page:

1.  Moved javascript scripts to bottom of body element
2.  Added Defer option to Google Analytics scripts to defer loading
3.  Removed OpenSans Google Font Link, Added Google Webfonts script to optimize font loading performance
4.  Minified Perfmatters.js, Inlined style.min.css
5.  Added async and media=print properties to print.css link
6.  Optimized image sizes for pizzeria.jpg, profilepic.jpg, and views/images/pizzeria.jpg (changed to pizzeria_sm.jpg)

These Optimizations have produced a 92 PageSpeed Mobile Score and a 94 Desktop Score.

#### Part 2: Optimize Frames per Second in pizza.html

The following optimizations were performed to get to 60 fps for the page scroll and less than 5 ms pizza resize time:

1.  Refactored change pizza sizes function for both simplification and to prevent a forced synchronous layout problem.
2.  Reduced the number of pizzas appended from 98 to 22.
3.  Added 'willchange: transform;' to style.css .mover element
4.  Added requestAnimationFrame to Scroll and DOMContentLoaded Event Listeners to help speed up pizza animations

These optimizations helped achieve 60 fps while scrolling the page and less than 5 ms response time for the pizza resizer.
