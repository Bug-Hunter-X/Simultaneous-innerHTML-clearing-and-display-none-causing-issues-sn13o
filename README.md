# Uncommon HTML Bug: Simultaneous innerHTML Clearing and display:none

This repository demonstrates an uncommon bug encountered when clearing the `innerHTML` of a div element and setting its `display` style to `none` simultaneously.  The issue manifests differently across browsers, potentially leading to unexpected behavior or rendering inconsistencies.

The bug is subtle and may not be immediately apparent. It's particularly noticeable when event listeners are attached to elements inside the div that is being manipulated.  Incorrect behavior may result from the unexpected order of execution or the browser's handling of the removal of elements while still in the DOM.

## Reproducing the Bug

1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Click the "Click Me" button.
4. Observe the behavior. The div might not completely disappear or subsequent attempts to manipulate the div may not work as expected.

## Solution

The provided solution in `bugSolution.html` addresses the issue by making the changes to the DOM sequentially instead of simultaneously.  This ensures that all changes are properly processed before the next change is made, resulting in expected and consistent behavior across different browsers.