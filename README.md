## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

####Part 1: Optimize PageSpeed Insights score for index.html
Optimizations done to index.html
- Combine all CSS for landing page into one file (main.css) with media queries for 'print' and 'portrait' and minify.
- Remove external link to Google Fonts.
- Add `async` to google-analytics.js and perfmatters.css javascript external references to allow for asynchronous parsing.
- Moved 'GoogleAnalyticsObject' inline script to end of html file since it isn't essential.
- Minified images.
- Add 'print' media query to print.css reference in index.html.

####Part 2: Optimize Frames per Second in pizza.html
Optimizations to Optimize FPS in pizza.html
- Removed determineDX function in main.js and optimized changePizzaSizes() function.
- Modified updatePositions() in main.js to reduce jank caused by repeated calls to document.body.scrollTop.
- Reduce the number of sliding pizza elements generated from 200 to 10.
- Reduced the sizes of pizza.png and pizzeria.jpg.
