# clojure-exercises

A bunch of simple exercises to get you started with Clojure.

## getting started

To work on the exercises you need a clojure environment. Here are
three recommended ways of getting one:

- Work on the exercises online at http://tryclj.com
- Nightcode is a nice and easy clojure IDE that you can install on
  Windows, OS X or Linux: https://sekao.net/nightcode/
- Or you can just simply download clojure from http://clojure.org
  and run it in your terminal for example like this:
  
  ```
  rlwrap java -jar clojure-1.8.0.jar
  ```

## useful stuff

To work on the exercises you'll need to refer to these materials:

- http://clojuredocs.org -- documentation for clojure functions (with examples!)
- http://clojure.org/reference -- long-form documentation about clojure concepts

## exercises

### syntax

1. compute `1+1`
1. call the function `get` with arguments `"ciao"` and `1`
1. compute `(3+4/5)*6`

1. define a _vector_ with the elements `1`, `"hello"` and `true`
1. define a vector that contains the _keywords_ `:diff` and `:merge`
1. define a _map_ with the key `1` is associated with the value `"hello"` and the key `:key`
   with the value `[13 7]`

1. use `def` to define a _variable_ `my-map` that refers to the map `{1 2}`.
   Use the `assoc` function to add a new key and value to `my-map`. What does
   the `assoc` call return?  What is the value of `my-map` after the call?

1. use the function `get` to get the second element from a vector
1. use the function `get` to get the value of a key from a map
1. get the value of a key from a map using the map itself as a function
1. get the value of a key from a map using a keyword as a function

1. use the function `get-in` to fetch the value `:treasure` from the value:

   ```clojure
   {:description "cave"
    :crossroads [{:contents :monster}
                 nil
                 {:contents [:trinket :treasure]}]}
   ```

1. use `defn` to define a function hello that works like this: `(hello) ==> "hello!"`
1. define a function `double` that works like this: `(double 5) ==> 10`, `(double 1) ==> 2`
1. add a _docstring_ to the function `double`. Then show it using `(doc double)`.

1. TODO: let, loop

### conditionals

1. define a function `small?` that returns `true` for numbers under 100
1. define a function `message!` that has three cases:

   ```clojure
   (message! :boink) ==> "Boink!"
   (message! :pig)   ==> "oink"
   (message! :ping)  ==> "pong"
   ```

1. reimplement `message!` using the `if` structure
1. reimplement `message!` using the `cond` structure
1. reimplement `message!` using the `case` structure

1. TODO?

### functional programming?

1. increment all the numbers in the vector `[4 7 9 10]` by one. Use
   the `map` funktiota. Hint: the function `inc`
1. do the same as in the previous exercise, but leave only the even results in the vector.
   Use the functions `filter` and `even?`

1. TODO

1. Use the funection `update-in` to change 3 into 4 in the value below:
   ```clojure
   {:shops [:shop-1]
    :customers [{:id "Pekka"
                 :account {:balance 3}}]}
   ```

1. TODO

1. challenge! use the `reduce` function to combine a vector of maps like this:
   ```clojure
   (combine [{:a 1 :b 2} {:c 3} {:d 4 :e 5}])
      ==> {:a 1 :b 2 :c 3 :d 4 :e 5}
   ```

### concurrency and parallelism

Atoms and refs are one of the coolest features of clojure, enabling
controlled mutation. This makes for safe & clear concurrent code.
Unfortunately I only have some basic exercises here, nothing with
concurrency.

1. define an _atom_ called `counter` that contains the value `4`
1. get the value of `counter` using the `@` operator
1. update `counter` to the value `5` with the function `reset!`
1. get the value of `counter` using the function `deref`
1. update `counter` to the value `6` by using the function `swap!`
   Hint: remember `inc`.

1. define a _ref_ called `account` that contains the value `4`
1. get the value of `account`
1. update `account` to the value `5` with the function `ref-set`.
   NB! you'll have to use the `dosync` macro
1. update `account` to the value `6` with the function `alter`

1. TODO: `pmap`, futures

### what next?

The website http://4clojure.com has lots of clojure exercises!
