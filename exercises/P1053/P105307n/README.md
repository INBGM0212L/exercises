# `P105307n` - Nagybetűk dekrementálása (`n` teszteset)

## A függvény
Írj egy `decrement_uppers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring nagybetűinek dekrementálásával kapunk!

### Magyarázat
Egy nagybetű dekrementálása alatt azt a műveletet értjük, mely során a betűt az ábécében őt megelőző nagybetűvel helyettesítjük. Például a `C` karaktert a `B` karakterre, míg a `B` karaktert az `A` karakterre cseréljük. Az `A` karaktert a `Z` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ZABCDEFGHIJKLMNOPQRSTUVWXY"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aZ······bA"` |
 | `"A··a·····b···B"` | `"Z··a·····b···A"` |
 | `"aB1cD2eF3gH4"` | `"aA1cC2eE3gG4"` |

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
ZABCDEFGHIJKLMNOPQRSTUVWXY
0123456789
a b c d e f g h
aZ      bA
Z  a     b   A
aA1cC2eE3gG4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
6
SDI8FY9c
LZFOQoBf1ij QVQXwFL
JDRSeWYokJSbH
TtWFAWVm6oLMVLR2zDQAKrIcVg
MPj1WMoMyPW5BOLHZ
ZTKPPAsXBQAG4gJl0r
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
RCH8EX9c
KYENPoAf1ij PUPWwEK
ICQReVXokIRbG
StVEZVUm6oKLUKQ2zCPZJrHcUg
LOj1VLoLyOV5ANKGY
YSJOOZsWAPZF4gIl0r
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
8
TfuQOHE9YcG5Qd6HNt
KFJRAEGWJ
DZiGXWMNL7N7GQVhHrEHaHKAoTbm
FTYPAQnKDZfCflB2HPA5S
CPVsDUOGZXw
ZD HMvQGFMyK
1DDDBFDh6
Y3D8BA7RJ
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
SfuPNGD9XcF5Pd6GMt
JEIQZDFVI
CYiFWVLMK7M7FPUhGrDGaGJZoSbm
ESXOZPnJCYfBflA2GOZ5R
BOUsCTNFYWw
YC GLvPFELyJ
1CCCAECh6
X3C8AZ7QI
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8
hJcUMVNFN6r gCGCAHduLY
Nu
6UO2OXnrjL7b
FBOtZqxQFJoFcaS
iKuvQeAom8xtipMDFn
Hr3uGFcMLWqPFHStBHFTXng
RRVXDrdRHXOIAHaGOPsJARXN DS
D0H7WhUwFwJgPnYJbMR7IKX8k
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
hIcTLUMEM6r gBFBZGduKX
Mu
6TN2NWnrjK7b
EANtYqxPEIoEcaR
iJuvPeZom8xtipLCEn
Gr3uFEcLKVqOEGRtAGESWng
QQUWCrdQGWNHZGaFNOsIZQWM CR
C0G7VhTwEwIgOnXIbLQ7HJW8k
```
