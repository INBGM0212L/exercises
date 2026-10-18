# `P105203t` - Nagybetűk duplikálása (végjelig olvasás)

## A függvény
Írj egy `double_uppers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring nagybetűinek megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"AABBCCDDEEFFGGHHIIJJKKLLMMNNOOPPQQRRSSTTUUVVWWXXYYZZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aAA······bBB"` |
 | `"A··a·····b···B"` | `"AA··a·····b···BB"` |
 | `"aB1cD2eF3gH4"` | `"aBB1cDD2eFF3gHH4"` |

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
abcdefghijklmnopqrstuvwxyz
AABBCCDDEEFFGGHHIIJJKKLLMMNNOOPPQQRRSSTTUUVVWWXXYYZZ
0123456789
a b c d e f g h
aAA      bBB
AA  a     b   BB
aBB1cDD2eFF3gHH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
UPaP
MTlPyWwFMMCPiZHLVAyqEKJ
XJ5AmcWZNMPP87ChEFl
OHABPQ5uQBQgV QOPWwuVDvBXQ
WQEgFcogwW
ITHdyHkB
EBBH6r4NTYYZiFRXJFAmlfV3WQ
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
UUPPaPP
MMTTlPPyWWwFFMMMMCCPPiZZHHLLVVAAyqEEKKJJ
XXJJ5AAmcWWZZNNMMPPPP87CChEEFFl
OOHHAABBPPQQ5uQQBBQQgVV QQOOPPWWwuVVDDvBBXXQQ
WWQQEEgFFcogwWW
IITTHHdyHHkBB
EEBBBBHH6r4NNTTYYYYZZiFFRRXXJJFFAAmlfVV3WWQQ
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
weZYzO88SB30PcIXpXG4ivojAFAYI
LLYSQU1pMJzMFcCM9dQGX
XTS
GUFSJbOEJX3QTcWcCHLh
IK92fbuBPPDW60aH0x
AHXCp
sEXIgjUJyRyhU
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
weZZYYzOO88SSBB30PPcIIXXpXXGG4ivojAAFFAAYYII
LLLLYYSSQQUU1pMMJJzMMFFcCCMM9dQQGGXX
XXTTSS
GGUUFFSSJJbOOEEJJXX3QQTTcWWcCCHHLLh
IIKK92fbuBBPPPPDDWW60aHH0x
AAHHXXCCp
sEEXXIIgjUUJJyRRyhUU
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8gACiKBSIg
PvmV4FPZ
E6LEO0DZ3XVVFo8j
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
8gAACCiKKBBSSIIg
PPvmVV4FFPPZZ
EE6LLEEOO0DDZZ3XXVVVVFFo8j
```
