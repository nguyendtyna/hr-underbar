# Underbar

This repo is an exercise to re-implement powerful and useful helper functions from the [Underscore.js](http://underscorejs.org/) library. The project was written in the same spirit as JavaScript Koans, and uses the [Mocha Test Suite](https://mochajs.org/) to faciliatate a TDD approach to learning. It walks through a reimplementation

## Additional Notes and Resources
- Work will be done in the ```underbar.js``` file
- Open ```SpecRunner.html``` in Chrome
- Many of the functions operate on "collections." They can take both arrays or objects as their arguments, and both cases need to be handled:
  - Use ```Array.isArray(obj)``` to find out whether an object is an array
  - Use ```obj.length``` to test if something is either a string or an array
- Javascript has a built-in ```Math``` object that provides some very useful functions
- Within a function, use the ```arguments``` keyword to access all the parameters that were passed in--even if they aren't named in the function definition. This is useful if the number of arguments being passed in in advance is unknown
  - Count the arguments by using ```arguments.length``` and access each argument using ```arguments[i]```
  - The ```arguments``` object is very similar to an array, but note that it does not support most array functions (such as ```slice``` or ```push```)
- If there is an array, ```myParameters```, and a function, ```myFunction```, using the elements in the array as parameters is to be called, use ```myFunction.apply(context, myParameters)```. The first parameter, ```context```, is the execution context for the function call. From inside myFunction, ```this``` can be accessed. For this exercise, just pass ```null``` for ```context```.

## Installation
[Pomander](https://github.com/hackreactor/precourse-pomander) will check the code for syntax errors and violations against the style guide before each commit. It uses a pre-commit hook to run staged files through ```eslint``` before each commit. ```eslint``` is a linter that will block commits should there be any syntax errors, or, should the style guide be violated. There are some preferred whitespace style rules that will give warnings but not block commits.

The following command is run from within the repository to install Pomander:

```curl -s https://raw.githubusercontent.com/hackreactor/precourse-pomander/master/bin/install | bash```

## Minimum Requirements
As is, the repository is missing code for most of the functions. The library must be fixed by implementing these functions. The functions are split into two sections, with a separate test suite for each. 

- The files in the ```spec``` directory contain the test suites. The goal is to get all the tests to pass by implementing the missing functions. 
- Run all the tests by opening ```SpecRunner.html``` in the browser.
- The file ```src/underbar.js``` contains function definitions and explanations for the following functions. Implement each of the functions by making all the tests pass:

Part I:
- [x] identity
- [x] first
- [x] last
- [x] each
- [x] indexOf
- [x] filter
- [x] reject
- [x] uniq
- [x] map
- [x] pluck
- [x] reduce

Part II:
- [x] contains
- [x] every
- [x] some
- [x] extend
- [x] defaults
- [x] once
- [x] memoize
- [x] delay
- [x] shuffle
