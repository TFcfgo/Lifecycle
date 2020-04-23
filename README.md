# R Function Badges

![](https://www.tidyverse.org/lifecycle/images/lifecycle.svg)

#### R funciton lifecycles & APIs <a id="api"></a>

This page describes the typical lifecycle of R functions at CFgO. Knowing where a function is in its lifecycle is particularly important for understanding how the API will change over time. The API \(short for application programming interface\) is the set of functions \(and their arguments\) that defines how you interact with the package.

#### Experimental![](.gitbook/assets/lifecycle-experimental.svg) <a id="experimental"></a>

An experimental function is in the very early stages of development. The API will be changing frequently as we rapidly iterate and explore variations in search of the best fit. Experimental functions are set up quickly without finished testing and documenting frameworks.

Every R function starts with the experimental badge.

#### Stable![](.gitbook/assets/lifecycle-stable.svg) <a id="stable"></a>

In a stable function, we are largely happy with the API, and major changes are unlikely. This means that the API will generally evolve by adding new functions and new arguments; we will avoid removing arguments or changing the meaning of existing arguments.

Conditions for functions marked as stable:

* Function in master branch
* Minimum testing framework set up and applied succesfully
* `roxygen2` function descriptions readable and understandable for anyone who did not programm the function
* At least one example applied to each function
* Example and testing results in 100% Code coverage checked by `covr`
* No future changes to the core of the function are expected - the function is ready for use in other packages

#### Deprected![](.gitbook/assets/lifecycle-deprecated%20%282%29.svg) <a id="archived"></a>

If API breaking change are needed, they will occur gradually. To begin with, the function or argument will be deprecated; it will continue to work but will emit an message informing you of the change. Next, typically after approx. 2 months, the message will be transformed to an error. Once all applications are checked and still work, the function will be removed.

Along with badge, add `rlang::warning()` to the function to remind all users of this function of the future remove. 

#### Questioning![](.gitbook/assets/lifecycle-questioning.svg) <a id="questioning"></a>

Functions which contain bugs, serve questionable purposes, contain slow / unexpected / unneccesarily complex code fragments or generate any further kind of unexpected behaviour.

Add a section "Questioning" at the end of the respective function. Use this to explain why the function in its current form is questioned. Additionaly, add an `rlang::warning()` to the function and generate `GitHub Issue` and link to GitHub to call attention to this issue.

