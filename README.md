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
1. TODO

### kontrollirakenteet

1. tee funktio `small?` joka palauttaa `true` luvuille alle 100
1. tee funktio `message!` jolla on kolme eri tapausta:

   ```clojure
   (message! :boink) ==> "Boink!"
   (message! :pig)   ==> "oink"
   (message! :ping)  ==> "pong"
   ```

1. toteuta funktio `message!` uudelleen käyttäen `if`-rakennetta
1. toteuta funktio `message!` uudelleen käyttäen `cond`-rakennetta
1. toteuta funktio `message!` uudelleen käyttäen `case`-rakennetta

### funktionaalista ohjelmointia

1. kasvata vektorin `[4 7 9 10]` kaikkia lukuja yhdellä. Käytä
   `map`-funktiota. Vihje: funktio `inc` kasvattaa lukua yhdellä!
1. tee sama kuin äsken, mutta jätä jäljelle vain parilliset luvut.
   Käytä funktioita `filter` ja `even?`

1. TODO

1. käytä funktiota `update-in` kasvattamaan numeroa 3 yhdellä alla
   olevassa rakenteessa:
   ```clojure
   {:shops [:shop-1]
    :customers [{:id "Pekka"
                 :account {:saldo 3}}]}
   ```

1. TODO

1. haastava: käytä `reduce`-funktiota yhdistämään vektori mappeja yhdeksi:
   ```clojure
   (combine [{:a 1 :b 2} {:c 3} {:d 4 :e 5}])
      ==> {:a 1 :b 2 :c 3 :d 4 :e 5}
   ```

### rinnakkaisuutta ja transaktioita

1. määrittele atomi `my-atom` joka sisältää arvon `4`
1. hae `my-atom`in nykyinen arvo operaattorilla `@`
1. päivitä `my-atom` arvoon `5` käyttämällä funktiota
   `reset!`
1. hae `my-atom`in nykyinen arvo funktiolla `deref`
1. päivitä `my-atom`in sisältämä arvo arvoon `6` käyttämällä funktiota
   `swap!`
1. määrittele ref `my-ref` joka sisältää arvon `4`
1. lue `my-ref`in arvo
1. päivitä `my-ref` arvoon `5` käyttämällä funktiota `ref-set`
   Huom: joudut käyttämään myös makroa `dosync`
1. päivitä `my-ref` arvoon 6 käyttämällä funktiota `alter`

### lopuksi

Vähän hankalampia tehtäviä tarjolla osoitteessa http://4clojure.com
