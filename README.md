# CSS Calc() Bug

This repository demonstrates a common bug related to using the `calc()` function in CSS. The issue arises when calculating a width based on the viewport width (`vw`) and subtracting a fixed value.  If the viewport width is smaller than the fixed value, the result becomes negative, causing unexpected rendering behavior.

The `bug.css` file contains the incorrect code. The `bugSolution.css` file provides a corrected implementation.

## How to reproduce

1. Open `bug.html` in a browser.
2. Resize the browser window to a very small width.
3. Observe the unexpected rendering of the element.

## Solution

The solution involves adding a `max()` function within the `calc()` expression to ensure that the calculated width is never negative. See `bugSolution.css` for the corrected code.