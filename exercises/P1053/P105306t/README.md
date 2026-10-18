# `P105306t` - Kisbetűk dekrementálása (végjelig olvasás)

## A függvény
Írj egy `decrement_lowers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring kisbetűinek dekrementálásával kapunk!

### Magyarázat
Egy kisbetű dekrementálása alatt azt a műveletet értjük, mely során a betűt az ábécében őt megelőző kisbetűvel helyettesítjük. Például a `c` karaktert a `b` karakterre, míg a `b` karaktert az `a` karakterre cseréljük. Az `a` karaktert a `z` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"zabcdefghijklmnopqrstuvwxy"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"z·a·b·c·d·e·f·g"` |
 | `"aA······bB"` | `"zA······aB"` |
 | `"A··a·····b···B"` | `"A··z·····a···B"` |
 | `"aB1cD2eF3gH4"` | `"zB1bD2dF3fH4"` |

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
END
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
zabcdefghijklmnopqrstuvwxy
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
z a b c d e f g
zA      aB
A  z     a   B
zB1bD2dF3fH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
nS IfBEqPPmvxrgQvglcowJvsjc
iNsvgzMwQawwtyOlzrfwiPY
GQyhf
R2yj w dF
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
mS IeBEpPPluwqfQufkbnvJurib
hNrufyMvQzvvsxOkyqevhPY
GQxge
R2xi v cF
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5IvRX7nU2lHaic
put2c2xsptlYFrwe2aajVsuk
Kt0jEaXTkVikgfw2d
SN
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
5IuRX7mU2kHzhb
ots2b2wroskYFqvd2zziVrtj
Ks0iEzXTjVhjfev2c
SN
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
sl1dywCg6TBaiwLi0ujisgulkCisr
mmKy
zdUTGbjzMd7yIkEytByb
6uaefbQgkGulaXgRmwalwkrJ
fRj9uXKriEjjwlwxevji
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
rk1cxvCf6TBzhvLh0tihrftkjChrq
llKx
ycUTGaiyMc7xIjExsBxa
6tzdeaQfjGtkzXfRlvzkvjqJ
eRi9tXKqhEiivkvwduih
```
