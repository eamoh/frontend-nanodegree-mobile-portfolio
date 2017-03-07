## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

####Part 1: Optimize PageSpeed Insights score for index.html
Optimizations done to index.html
1. Combine all CSS for landing page into one file (main.css) with media queries for 'print' and 'portrait' and minify.
2. Remove external link to Google Fonts.
3. Add `async` to google-analytics.js and perfmatters.css javascript external references to allow for asynchronous parsing.
4. Moved 'GoogleAnalyticsObject' inline script to end of html file since it isn't essential.
5. Minified images.
6. Add 'print' media query to print.css reference in index.html.

####Part 2: Optimize Frames per Second in pizza.html
Optimizations to Optimize FPS in pizza.html
1. Removed determineDX function in main.js and optimized changePizzaSizes() function.
2. Modified updatePositions() in main.js to reduce jank caused by repeated calls to document.body.scrollTop.
