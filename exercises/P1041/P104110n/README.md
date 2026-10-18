# `P104110n` - Növekvő szomszédok száma (`n` teszteset)

## A függvény
Írj egy `count_of_increasing_neighbours` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott listában hány olyan elem van, mely nagyobb az őt megelőzőnél!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[89, 41, 99, -14, -90, 4, 85, -32]` | `3` |
 | `[90, -76, 5]` | `1` |
 | `[-63, 35, 65, 76, -30, -63, -40, -4]` | `5` |
 | `[11, 40, 43, -61, 64, -52, -26, 51, -42, 66]` | `6` |
 | `[79]` | `0` |
 | `[-70]` | `0` |
 | `[-84, 47, -26]` | `1` |
 | `[-26, -96, -82, 57, 32]` | `2` |
 | `[27, -35, 12, 25, -58, 40, 43, 76, 57, -4]` | `5` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a feldolgozandó lista (`numbers`) elemei szerepelnek egy-egy szóközzel elválasztva egymástól.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy második, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
9
89 41 99 -14 -90 4 85 -32
90 -76 5
-63 35 65 76 -30 -63 -40 -4
11 40 43 -61 64 -52 -26 51 -42 66
79
-70
-84 47 -26
-26 -96 -82 57 32
27 -35 12 25 -58 40 43 76 57 -4
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
3
1
5
6
0
0
1
2
5
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
6
75 -28 -31 -56 82 -30 56
-33 32 49 48 -24 -16
-70 56 -69
-28 -28 55 -28 9 91
-88 -50 68 78 37 -56 6
22 15 -16 -58 -86 45 7 -12
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
2
3
1
3
4
1
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
7
-30 4 -40
77 -31 11 61 48 86 -33 38 59
-49 -37 89 -66 -30 -57
19 17 83
-34 -15 43 -43 -63 -45 23 -81
-87 -72
-20 -54 44
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
1
5
3
1
4
1
1
```
