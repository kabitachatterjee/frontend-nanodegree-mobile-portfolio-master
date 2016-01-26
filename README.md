## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

1. The project is hosted on gh-pages.
2. Open the link [http://kabitachatterjee.github.io/frontend-nanodegree-mobile-portfolio-master/] in your browser.
3. Copy the URL and try running it through PageSpeed Insights.It gives a score of 95 for mobile and 97 for desktop.

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, views/js/main.js was modified at the following places:

1. Line 424 - 445 - The functions determineDx(elem,size) and sizeSwitcher(size) were removed.
The for loop inside the function changePizzaSizes(size) was making several iterative calls to the function determineDx and making layout and style changes again and again within the loop. Instead we changed the logic within the for loop to make it simpler with no iterative function calls. 

2. Line 486 - 515 - The function updatePositions() was modified such that the complex Math.sin() calculations are done outside the for loop.