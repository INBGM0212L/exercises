# `P105303e` - Számjegyek inkrementálása (állományvégjelig olvasás)

## A függvény
Írj egy `increment_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring számjegyeinek inkrementálásával kapunk!

### Magyarázat
Egy számjegy inkrementálása alatt azt a műveletet értjük, mely során a számjegyet az érték szerint őt követő számjeggyel helyettesítjük. Például a `0` karaktert az `1` karakterre, míg az `1` karaktert a `2` karakterre cseréljük. A `9` karaktert az `0` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"1234567890"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB2cD3eF4gH5"` |

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
1234567890
a b c d e f g h
aA      bB
A  a     b   B
aB2cD3eF4gH5
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
O4m788Kb758L56KoOaY3Bt19
A7ue9
0oQMa8
SB575n2o622978514
g6Oh6G26Ep3m55D4835k
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
O5m899Kb869L67KoOaY4Bt20
A8ue0
1oQMa9
SB686n3o733089625
g7Oh7G37Ep4m66D5946k
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
bG4 ED9G82
s5S1E5iNU579S00E154S5
 FQ3665x0g87oC10N14rT1E7
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
bG5 ED0G93
s6S2E6iNU680S11E265S6
 FQ4776x1g98oC21N25rT2E8
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
n5QUB319q2l0I0IX1wz0F82ws
8nW7vV230Jd9o640Wi08U2g38
Gg
59Qyz29J5x79mb
0Ozda6nb
g341493G5j06AE
HrWFAs96Rgw5kAwrbI5F0pu9k
1U90h7j781s330Ltl869d1I1hoH
264C4f
sF28N4H4Dg5b2cq54vw
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
n6QUB420q3l1I1IX2wz1F93ws
9nW8vV341Jd0o751Wi19U3g49
Gg
60Qyz30J6x80mb
1Ozda7nb
g452504G6j17AE
HrWFAs07Rgw6kAwrbI6F1pu0k
2U01h8j892s441Ltl970d2I2hoH
375C5f
sF39N5H5Dg6b3cq65vw
```
