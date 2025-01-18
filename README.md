# Uncommon HTML Bug: Unexpected innerHTML Behavior

This repository demonstrates a subtle bug related to manipulating HTML content using `innerHTML`.  The issue arises from the repeated use of `innerHTML` on the same element in different lines.

## Bug Description

The `bug.html` file contains a simple HTML structure with a div element and some JavaScript code.  The JavaScript attempts to append new content to the div using `innerHTML`. While the first append works correctly, the second one is inconsistent across browsers. This inconsistency stems from how different browsers handle multiple `innerHTML` assignments to the same element in the same block of code, sometimes resulting in unexpected behavior or errors.

## Solution

The `bugSolution.html` file provides a corrected version.  The solution uses a more reliable approach to manipulate the DOM, such as using `insertAdjacentHTML`, `appendChild`, or creating the element and then appending it. This method ensures consistent behavior across different browsers.