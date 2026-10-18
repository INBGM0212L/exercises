# `P105102e` - Kisbetűk eltávolítása (állományvégjelig olvasás)

## A függvény
Írj egy `delete_lowers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring kisbetűinek törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `""` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"·······"` |
 | `"aA······bB"` | `"A······B"` |
 | `"A··a·····b···B"` | `"A··········B"` |
 | `"aB1cD2eF3gH4"` | `"B1D2F3H4"` |

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

ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
       
A      B
A          B
B1D2F3H4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
hmkaolbVhk2z6gdvxrnUq7l8hRM
CaTm1atqlm2eobjjFslQDU
lWr2
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
V26U78RM
CT12FQDU
W2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
x lv
mbNElznxysOe4lf5Hyqb7s
hd
bo
rlukkcFfMMTglznSNecuFYr5YDp
fJb xs7AvlepoRwbkgn
wqOGjoiqQb
qXikhubfEYfveqEXgwtL6YpCulsfff
DXMIi7ck
tdc
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
 
NEO45H7


FMMTSNFY5YD
J 7AR
OGQ
XEYEXL6YC
DXMI7
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
chow5nS7f3tbzX5063ucl8ak
ox5edwvulsFoAk9cej
bCpfJAaniemy
zthriZ
qOlnLszbtApeiL5wrahe
KpSiephINEqoTURJorvh6H
0nkcmyWZj8vhbZSsvMfjh53cf6kwuz
xAn0hl3DK1u
XZ8ZdkdIBWjs9dojkcvBP6vJPnVoym
lGqqdzfg
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
5S73X50638
5FA9
CJA
Z
OLAL5
KSINETURJ6H
0WZ8ZSM536
A03DK1
XZ8ZIBW9BP6JPV
G
```
