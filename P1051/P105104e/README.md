# `P105104e` - Számjegyek eltávolítása (állományvégjelig olvasás)

## A függvény
Írj egy `delete_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring számjegyeinek törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `""` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aBcDeFgH"` |

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

a b c d e f g h
aA      bB
A  a     b   B
aBcDeFgH
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
467I724ty7
7
FhS1c27a2ns65d
N06TVN7CpI4y7Llk
94301r63Fg135ynB5D7Og341AO3
02N04BtH5063MQzvLG0892
cOIks4O359HPHJb70eQ
86WGO8yYI9iIh8gN31
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
Ity

FhScansd
NTVNCpIyLlk
rFgynBDOgAO
NBtHMQzvLG
cOIksOHPHJbeQ
WGOyYIiIhgN
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
42htpaQZj0lgDB1nJH7U
sjg73I98b97N877di01j
3EV1t6D7KBy3B6
uFDwu687uCvqdB04G94 03l9490
9oznvs
43865qLxDn6O27
L8821862M104U09CaH1c4aj724h3
0Em7K666a08m37jLfW800WI 
C
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
htpaQZjlgDBnJHU
sjgIbNdij
EVtDKByB
uFDwuuCvqdBG l
oznvs
qLxDnO
LMUCaHcajh
EmKamjLfWWI 
C
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
374C0
0742kXL44509zRx3301z51552I03
MJX7HO Q6f65u3
Tg7
3593OX74ku37 
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
C
kXLzRxzI
MJXHO Qfu
Tg
OXku 
```
