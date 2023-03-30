---
layout: page
title: Tidier.jl
description: Julia implementation of the R tidyverse
img: assets/img/Tidier_jl_logo.png
importance: 1
category: Research
---

I'm actively contributing to [Tidier.jl](https://github.com/kdpsingh/Tidier.jl), which is an open source projected maintained by my faculty advisor: [Dr. Karandeep Singh](https://kdpsingh.lab.medicine.umich.edu/).

`Tidier.jl` is a 100% Julia implementation of the R tidyverse mini-language in Julia. Powered by the `DataFrames.jl` package and Julia’s extensive meta-programming capabilities, Tidier.jl is an R user’s love letter to data analysis in Julia.

`Tidier.jl` has three goals, which differentiate it from other data analysis meta-packages in Julia:

1. **Stick as closely to tidyverse syntax as possible:** Whereas other meta-packages introduce Julia-centric idioms for working with DataFrames, this package’s goal is to reimplement parts of tidyverse in Julia. This means that Tidier.jl uses tidy expressions as opposed to idiomatic Julia expressions. An example of a tidy expression is `a = mean(b)`.

2. **Make broadcasting mostly invisible:** Broadcasting trips up many R users switching to Julia because R users are used to most functions being vectorized. `Tidier.jl` currently uses a lookup table to decide which functions not to vectorize; all other functions are automatically vectorized. Read the documentation page on "Autovectorization" to read about how this works, and how to override the defaults.

3. **Make scalars and tuples mostly interchangeable:** In Julia, the function `across(a, mean)` is dispatched differently than `across((a, b), mean)`. The first argument in the first instance above is treated as a scalar, whereas the second instance is treated as a tuple. This can be very confusing to R users because `1 == c(1)` is `TRUE` in R, whereas in Julia `1 == (1,)` evaluates to `false`. The design philosophy in `Tidier.jl` is that the user should feel free to provide a scalar or a tuple as they see fit anytime multiple values are considered valid for a given argument, such as in `across()`, and `Tidier.jl` will figure out how to dispatch it.
