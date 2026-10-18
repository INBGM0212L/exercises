# `P105108e` - Páratlan számjegyek eltávolítása (állományvégjelig olvasás)

## A függvény
Írj egy `delete_odd_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páratlan számjegyeinek törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"02468"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aBcD2eFgH4"` |

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
02468
a b c d e f g h
aA      bB
A  a     b   B
aBcD2eFgH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
jD7h11M7Ob7 mWpV56
ypO3sfYNqVg9vsDu7y
Gh979759N53mb5N5
W9d 17qdPt9uSG79LQVM99FJH3RRv
 b12LN5xA55MA59
7cMZ7pDk5SX719pXR231J151D
05cjp1TDwSl7h1735619R1b14hN
W05Hv5ceFr7L551LQI1DFXw
Mkmjq
9333v07OD5ssp
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
jDhMOb mWpV6
ypOsfYNqVgvsDuy
GhNmbN
Wd qdPtuSGLQVMFJHRRv
 b2LNxAMA
cMZpDkSXpXR2JD
0cjpTDwSlh6Rb4hN
W0HvceFrLLQIDFXw
Mkmjq
v0ODssp
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
93TTkVAW73N
U
17w0Zt715S6Kl7pFm1Xwa95Nmiy7R
tsNgcDwgIO7a
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
TTkVAWN
U
w0ZtS6KlpFmXwaNmiyR
tsNgcDwgIOa
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
f51 5n3vnH9DuAJ17vQtE9i u39a05
31wp5Lv1nbo77e7mO9Qi1ZT5RO
L1F13F5NG29jbZ3dfo1411x353Bh7
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
f nvnHDuAJvQtEi ua0
wpLvnboemOQiZTRO
LFFNG2jbZdfo4xBh
```
