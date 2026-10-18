# `P105308n` - Számjegyek dekrementálása (`n` teszteset)

## A függvény
Írj egy `decrement_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring számjegyeinek dekrementálásával kapunk!

### Magyarázat
Egy számjegy dekrementálása alatt azt a műveletet értjük, mely során a számjegyet az érték szerint őt megelőző számjeggyel helyettesítjük. Például a `2` karaktert az `1` karakterre, míg az `1` karaktert a `0` karakterre cseréljük. A `0` karaktert a `9` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"9012345678"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB0cD1eF2gH3"` |

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
ABCDEFGHIJKLMNOPQRSTUVWXYZ
9012345678
a b c d e f g h
aA      bB
A  a     b   B
aB0cD1eF2gH3
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
8
58NA077
19
0o5j276IEVS180M7fJk94738809Xx3
17fhE81K
6P0QVr2S9n219r595v1j41R
q2Ojfxt171J32d05zB
x53k5137m608qk7 
v714 j5x9k 
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
47NA966
08
9o4j165IEVS079M6fJk83627798Xx2
06fhE70K
5P9QVr1S8n108r484v0j30R
q1Ojfxt060J21d94zB
x42k4026m597qk6 
v603 j4x8k 
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
6
09ZEY88BQc35
4Ow3
BNZg7FR4x96F8X0G
ijO115a92N387Pi3ZC8mt0i6
6l38CZ219wtl22M1Hyg
S0R2g78XdlMH04j4
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
98ZEY77BQc24
3Ow2
BNZg6FR3x85F7X9G
ijO004a81N276Pi2ZC7mt9i5
5l27CZ108wtl11M0Hyg
S9R1g67XdlMH93j3
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
10
38U37x8bG1 3 8
10Po2P3CW7O0z2R0
3U88rc97a5v8oLxRv2
Y4U8061i6UQ9Pu63Agc2Iw7Nq1wn5
134Ad
7LdtQ
O09sQP33S63c
241uv1O2B7AAyt94u6cV
2b26r360
Gm62O48795UG
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
27U26x7bG0 2 7
09Po1P2CW6O9z1R9
2U77rc86a4v7oLxRv1
Y3U7950i5UQ8Pu52Agc1Iw6Nq0wn4
023Ad
6LdtQ
O98sQP22S52c
130uv0O1B6AAyt83u5cV
1b15r259
Gm51O37684UG
```
