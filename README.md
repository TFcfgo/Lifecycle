# Lifecycle

![](https://www.tidyverse.org/lifecycle/images/lifecycle.svg)

#### Package lifecycles & APIs <a id="api"></a>

This page describes the typical lifecycle on an R package. Knowing where a package is in its lifecycle is particularly important for understanding how the API will change over time. The API \(short for application programming interface\) is the set of functions \(and their arguments\) that defines how you interact with the package.

There are three ways an API can change:

1. It can **grow** when a function or argument is added.
2. It can **shrink** when a function or argument is removed.
3. It can **change** when the meaning of an argument changes, or the type of data returned from a function changes.

Changing or shrinking the API will **break** it: code that previously worked will no any longer. \(Sometimes code will break even if the API doesn’t; for example, you might have accidentally depended on behaviour that the author thought was a bug\).

#### Experimental![](https://img.shields.io/badge/lifecycle-experimental-orange.svg) <a id="experimental"></a>

An experimental package or function is in the very early stages of development. The API will be changing frequently as we rapidly iterate and explore variations in search of the best fit. Experimental packages / functions are set up quickly without finished testing and documenting frameworks.

#### Stable![](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg) <a id="stable"></a>

In a stable package, we are largely happy with the API, and major changes are unlikely. This means that the API will generally evolve by adding new functions and new arguments; we will avoid removing arguments or changing the meaning of existing arguments.

If API breaking change are needed, they will occur gradually. To begin with, the function or argument will be deprecated; it will continue to work but will emit an message informing you of the change. Next, typically after at least a year, the message will be transformed to an error.

#### Deprected![](.gitbook/assets/lifecycle-deprecated%20%282%29.svg) <a id="archived"></a>

The development of an archived package is complete, and it has been archived on CRAN and on GitHub.

#### Dormant![](https://img.shields.io/badge/lifecycle-dormant-blue.svg) <a id="dormant"></a>

A dormant package is not completed, but is not currently under active development. We plan to return to it in the future.

#### Questioning![](https://img.shields.io/badge/lifecycle-questioning-blue.svg) <a id="questioning"></a>

We are no longer convinced that a questioning package is the optimal approach, but we don’t yet know what a better approach is.

