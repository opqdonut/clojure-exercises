# clojure-harjoituksia

## syntaksi

1. laske `(3+4/5)*6`
1. kutsu funktiota `get` argumenteilla `"ciao"` ja `1`

1. määrittele vektori jossa on elementit `1`, `"moi"` ja `true`
1. määrittele vektori joka sisältää keywordit `:diff` ja `:merge`
1. määrittele map jossa avain `1` liittyy arvoon `"hei"` ja avain `:key`
   arvoon `[13 7]`

1. määrittele muuttuja `my-map` joka sisältää mapin `{1 2}`. Lisää
   `my-map`piin `assoc`-funktiolla uusi avain ja arvo. Mitä `assoc`-funktio
   palauttaa? Mikä on `my-map` muuttujan arvo tämän jälkeen?

1. käytä funktiota `get` hakemaan vektorin toinen alkio
1. käytä funktiota `get` hakemaan mapista avain
1. hae mapista avain käyttämällä itse mappia funktiona
1. hae mapista avain käyttämällä keywordiä funktiona 

1. Käytä funktiota get-in noutamaan arvo `:aarre` arvosta:

```
{:kuvaus "luolasto"
 :risteys [{:sisalto :hirvio}
           nil
           {:sisalto [:hely :aarre]}]}
```

1. tee funktio hello joka toimii näin: `(hello) ==> "hello!"`
1. tee funktio tupla joka toimii näin: `(tupla 5) ==> 10, (tupla 1) ==> 2`

...

## kontrollirakenteet

1. tee funktio `small?` joka palauttaa `true` luvuille alle 100
1. tee funktio `message!` jolla on kolme eri tapausta:
```
(message! :boink) ==> "Boink!"
(message! :pig)   ==> "oink"
(message! :ping)  ==> "pong"
```
1. toteuta funktio `message!` uudelleen käyttäen `if`-rakennetta
1. toteuta funktio `message!` uudelleen käyttäen `cond`-rakennetta
1. toteuta funktio `message!` uudelleen käyttäen `case`-rakennetta

## funktionaalista

1. kasvata vektorin `[4 7 9 10]` kaikkia lukuja yhdellä. Käytä
   `map`-funktiota. Vihje: funktio `inc` kasvattaa lukua yhdellä!
1. tee sama kuin äsken, mutta jätä jäljelle vain parilliset luvut.
   Käytä funktioita `filter` ja `even?`

...

1. käytä funktiota `update-in` kasvattamaan numeroa 3 yhdellä alla
   olevassa rakenteessa:
```
{:shops [:shop-1]
 :customers [{:id "Pekka"
              :account {:saldo 3}}]}
```

...

1. haastava: käytä `reduce`-funktiota yhdistämään vektori mappeja yhdeksi:
```
(combine [{:a 1 :b 2} {:c 3} {:d 4 :e 5}])
   ==> {:a 1 :b 2 :c 3 :d 4 :e 5}
```

## rinnakkaisuutta ja transaktioita

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

## lopuksi

Vähän hankalampia tehtäviä tarjolla osoitteessa http://4clojure.com
