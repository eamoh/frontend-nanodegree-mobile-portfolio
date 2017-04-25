## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

#### Part 1: Steps Required to Run the Application
- The _app_ folder contains the source files and the _dist_ folder contains the files served to the website
- Install and run gulp dependencies in root folder. Install [here](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md).
- Install [ngrok](https://ngrok.com/) to provide secure tunnels to localhost and allow you to use PageSpeed Insights. Install ngrok in the _dist_ folder and run it from there.
- Navigate to the _dist_ folder and run the local Python server from the terminal by typing in the following code: `python -m SimpleHTTPServer`.

#### Part 2: Optimize PageSpeed Insights score for index.html
Optimizations done to index.html
- Inline all of styles.css and add "print" media query to print.css HTML reference
- Remove external link to Google Fonts.
- Concatenate, minify and add `async` to google-analytics.js and perfmatters.css javascript external references to allow for single call and asynchronous parsing.
- Moved 'GoogleAnalyticsObject' inline script to end of html file since it isn't essential.
- Minified images.

#### Part 3: Optimize Frames per Second in pizza.html
Steps to Optimize FPS in pizza.html
- Removed determineDX function in main.js and optimized changePizzaSizes() function.
- Modified updatePositions() in main.js to reduce jank caused by repeated calls to document.body.scrollTop.
- Reduce the number of sliding pizza elements generated from 200 to an automatically calculating the number of scrolling pizzas needed based on the user's screen height.
- Minify pizza.html, CS and JS files
