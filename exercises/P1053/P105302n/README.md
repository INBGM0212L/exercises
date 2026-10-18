# `P105302n` - Nagybetűk inkrementálása (`n` teszteset)

## A függvény
Írj egy `increment_uppers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring nagybetűinek inkrementálásával kapunk!

### Magyarázat
Egy nagybetű inkrementálása alatt azt a műveletet értjük, mely során a betűt az ábécében őt követő nagybetűvel helyettesítjük. Például az `A` karaktert a `B` karakterre, míg a `B` karaktert a `C` karakterre cseréljük. A `Z` karaktert az `A` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"BCDEFGHIJKLMNOPQRSTUVWXYZA"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aB······bC"` |
 | `"A··a·····b···B"` | `"B··a·····b···C"` |
 | `"aB1cD2eF3gH4"` | `"aC1cE2eG3gI4"` |

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
7
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
BCDEFGHIJKLMNOPQRSTUVWXYZA
0123456789
a b c d e f g h
aB      bC
B  a     b   C
aC1cE2eG3gI4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
3
J5V4JlVsX9T
EQZ7ZOZYNS4nzXC9AYIb3mMMZHO
BdSmQK
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
K5W4KlWsY9U
FRA7APAZOT4nzYD9BZJb3mNNAIP
CdTmRL
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5
Y9UKIKFg1qQL4lFJQCFUDSSSSE
G9XhfYZ6QJUNsSLHEZIMtW QOoOPZa
QD1J
OQSNVkTDeEJTZOIOOHU
LKdKZeMDMXRKtUUNCLHAnUNMEE
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
Z9VLJLGg1qRM4lGKRDGVETTTTF
H9YhfZA6RKVOsTMIFAJNtX RPoPQAa
RE1K
PRTOWkUEeFKUAPJPPIV
MLdLAeNENYSLtVVODMIBnVONFF
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8
jHIT0QDpCVRkWRySCeIhSPCWEZI
4OGFWdBJGgLYE6YFo
WfoFXkDLhH
k
yZYQXUTIKPTEJ9XY8HBBBV
kR4AHP0P3WCqPBR KzFdNdMECQvG
N8fTGwJ WSJ08YdrTSpeetOXQSLKB6
D4oGUC62RQEAWOnlGHFAWYNRHY5
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
jIJU0REpDWSkXSyTDeJhTQDXFAJ
4PHGXdCKHgMZF6ZGo
XfoGYkEMhI
k
yAZRYVUJLQUFK9YZ8ICCCW
kS4BIQ0Q3XDqQCS LzGdOdNFDRvH
O8fUHwK XTK08ZdrUTpeetPYRTMLC6
E4oHVD62SRFBXPnlHIGBXZOSIZ5
```
