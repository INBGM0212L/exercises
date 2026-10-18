# `P105101e` - Szóközök eltávolítása (állományvégjelig olvasás)

## A függvény
Írj egy `delete_spaces` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring szóközeinek törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"abcdefgh"` |
 | `"aA······bB"` | `"aAbB"` |
 | `"A··a·····b···B"` | `"AabB"` |
 | `"aB1cD2eF3gH4"` | `"aB1cD2eF3gH4"` |

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
0123456789
abcdefgh
aAbB
AabB
aB1cD2eF3gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
78whLQGsQ
FTl B34LxT dzpXxDHl dj
t9 tv  aoNqh lVfWahYUHQdM 
Mk  eZ PxYl r 
UV8S4tzo 
AfU zqmbl  utiar
Fk8yT
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
78whLQGsQ
FTlB34LxTdzpXxDHldj
t9tvaoNqhlVfWahYUHQdM
MkeZPxYlr
UV8S4tzo
AfUzqmblutiar
Fk8yT
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
jp mp
tw
5vV65qn vKAx9d9mmW
   KaNS4  AvQWkqHmwA0QZ3
N  NWsAMBY 
 WN1TVHcZQzMzcU
JuuntpeVAvFDMmK  Ff
  afm2 EUbhVCN G hBmPRp  lUfd
nn m pxc qv 6 hQaxf1
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
jpmp
tw
5vV65qnvKAx9d9mmW
KaNS4AvQWkqHmwA0QZ3
NNWsAMBY
WN1TVHcZQzMzcU
JuuntpeVAvFDMmKFf
afm2EUbhVCNGhBmPRplUfd
nnmpxcqv6hQaxf1
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
9jM
48 84u JcQjLagMsfeU v5FB1t
PNEBSdyT m ml   puDy p
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
9jM
4884uJcQjLagMsfeUv5FB1t
PNEBSdyTmmlpuDyp
```
