# `P105107e` - Páros számjegyek eltávolítása (állományvégjelig olvasás)

## A függvény
Írj egy `delete_even_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páros számjegyeinek törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"13579"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB1cDeF3gH"` |

A paraméterekhez tartozó literálokban minden `' '` (szóköz) karakter a `'·'` (pont) karakterrel kerül helyettesítésre.


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`original`) szerepel.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
a b c d e f g h
aA      bB
A  a     b   B
aB1cD2eF3gH4
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
13579
a b c d e f g h
aA      bB
A  a     b   B
aB1cDeF3gH
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
T8MuOPQQbUq43Lx0He
D02
gi
diX8U0D0
XrGX0663 R7
4084HL924w0y624Ay8w646
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
TMuOPQQbUq3LxHe
D
gi
diXUD
XrGX3 R7
HL9wyAyw
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
2dG0B6xz0SWnm4D8Jro80AAPa0K
O6Z942IzB0486E0D6u8og0gwF444
0K640q8B4b
2wRIxKmRQi5q2lCmQvB20ohq9x2c
02r828864lH646JB662
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
dGBxzSWnmDJroAAPaK
OZ9IzBEDuoggwF
KqBb
wRIxKmRQi5qlCmQvBohq9xc
rlHJB
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
587k8vQa84pF88h0Xz808n82S
GHn4cRJ0022hg4Q2820e82EE2
ch43qW88473KX24Xv6 H6287lQ
6806b49GCN5yk52ll4H6qe322n0624
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
57kvQapFhXznS
GHncRJhgQeEE
ch3qW73KXXv H7lQ
b9GCN5yk5llHqe3n
```
