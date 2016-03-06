# Web Site Optimization Challenge

## About

This project was presented as a challenge to optimize the performance of the front page and the pizza page. The front page had to run with a PageSpeed score of 90 on desktop and mobile.

The Pizza page had to run at a consistent 60 FPS while scrolling and the time to re-size the pizzas had to run in less than 5 ms.

To view the website go to http://peleus.github.io/OptimizedWebSite/.

## My Optimizations

Index.HTML

Optimizations included:
- Removing the Google font reference seemed to help performance. Removing it did not seem to substantially change the appearance of the text. It did cause performance issues.
- I moved the CSS link to the bottom of the page. This seemed to improve performance substantially with no substantial visual issues.
- I deferred the Google Analytics JavaScript.
- I optimized the size of the page raster files.
- The page now has a mobile PageSpeed score of 93 and a desktop score of 93.

main.js

Optimizations included:
- In the function changePizzaSizes I pulled out query var assignments that did not make use of the loop iteration.
- In the function determineDx I moved two assignments to outside of the loop of the calling function and then passed them in as parameters.
- In function updatePositions I removed several variable assignments from inside the loop that were causing a reflow on each iteration.
- In function updatePositions I re-factored to use a transformX rather than updating an offset that was causing a reflow.