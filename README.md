# Week 6 Saturday Exercises

8/3/19
Problem Definition is below. This is my solution to the exercises associated with tracking down bugs in code.

I will utilize the bug reports in my effort, but I have been warned that even bug reports can give false information.

1 - console error suggested an unexpected token on index.js:7. found a string which was unclosed
2 - console error.. linked js files not found. The src for each script had the wrong path
3 - bug-report.txt said .new:hover wasn't working. I found an inline style blocking the psuedoclass selector. Moved the inline style to the 'less specific' `.new` selector
4 - results filter should be case insensitive. Modified the compare values to all lower case to force match regardless of case
5 - no styling. console says css file not found. style href attribute had wrong path
6 - console says `transaction` not defined on index.js:12. Found that the code was iterating through an array of transactions, so semantically it made sense to look at the parameter of the anonymous function and the `transaction` variable was missing.
7 - bug report says there is a ',' before each transaction. Found that the renderTransactions function is joining an array of HTML code pieces. Array.prototype.join() defaults to separating each element with ", ", so I specified the delimiter to ''
8 - filter is only doing on ENTER. Every keypress should update filter result. Found in filterResults that the event handler was hooked into `onchange` but this doesn't fire on each character input; changed to hoooking into `oninput`

Exercises complete =). It is interesting how different it can be tracking down runtime errors vs application-level bugs.

# skware-cash

Welcome! Skware Cash is a simple clone of Square Cash designed to be a playground for Chrome DevTools. Please note that this isn't a complete clone - only the transactions list has been rebuilt.

You will find 8 folders named "bug". Each of them contain nearly identical copies of these 5 files:

- bug-report.txt
- index.html
- index.css
- index.js
- data.js

Your task is to discover and patch the bugs in each of the bug folders! Begin by reading the bug-report.txt and then using Chrome's DevTools to uncover the bug's underlying issue.

The last two bugs are a bit tough! Remember, Google is your friend - don't be afraid to search the web for possible solutions.
