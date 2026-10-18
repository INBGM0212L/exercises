# `P104113n` - Nemcsökkenő szomszédok száma (`n` teszteset)

## A függvény
Írj egy `count_of_non_decreasing_neighbours` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott listában hány olyan elem van, mely nem kisebb az őt megelőzőnél!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[1, 22]` | `1` |
 | `[-19, 10, -87, 12, 51, 91, -3, 4, -51]` | `5` |
 | `[-63, 23, -82, -41, -80, 16, 41, 40, 88]` | `5` |
 | `[-54, -61, 70, -46, 73, -63, -69]` | `2` |
 | `[-29, -58, -70, -73, 62, 28, -57, 50]` | `2` |
 | `[-85, 12, 63, -6, -24, -58]` | `2` |
 | `[10, 62, -16, -64, -60, -98, 35, 50]` | `4` |
 | `[-54, -80]` | `0` |
 | `[49, 2, -68, -65, -58, -10, -57]` | `3` |


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
1 22
-19 10 -87 12 51 91 -3 4 -51
-63 23 -82 -41 -80 16 41 40 88
-54 -61 70 -46 73 -63 -69
-29 -58 -70 -73 62 28 -57 50
-85 12 63 -6 -24 -58
10 62 -16 -64 -60 -98 35 50
-54 -80
49 2 -68 -65 -58 -10 -57
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1
5
5
2
2
2
4
0
3
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5
-16 -95 71 82 38 8
61 -50 89 16 -92 88 -37 5
-16
6 -5 51 24 -89 -82 -61 73
30 -95 -2 86 40 81 83 99 89 -55
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
2
3
0
4
5
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
4
-52
-96 -90
47 76 -67 42
-69 78 86 -6 -70
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
0
1
2
2
```
