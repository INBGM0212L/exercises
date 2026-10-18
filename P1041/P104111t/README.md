# `P104111t` - Csökkenő szomszédok száma (végjelig olvasás)

## A függvény
Írj egy `count_of_decreasing_neighbours` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott listában hány olyan elem van, mely kisebb az őt megelőzőnél!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[10, 63, 45, -68]` | `2` |
 | `[55, -67, 93, -26, -55, 0, 40, 81, -92, 50]` | `4` |
 | `[-12, -47, -61, -97, 30, -57, -37, -35, 40, -91]` | `5` |
 | `[65, -61, 27, 0, 61, 46]` | `3` |
 | `[-95, -2, 84, -67, -58, -77, 95]` | `2` |
 | `[6, 62, 34, -86, -76, -80, -54]` | `3` |
 | `[52, -12, -28, -46, 46, -91]` | `4` |
 | `[-67, 94, -38, 98, -68, 3, -28, 57, -77, 38]` | `4` |
 | `[54, 29, 31, 10, 77, -10, 64]` | `3` |
 | `[96, 34, -43]` | `2` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét egy üres sor (`""`) jelzi (melyet már nem kell feldolgozni).
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
10 63 45 -68
55 -67 93 -26 -55 0 40 81 -92 50
-12 -47 -61 -97 30 -57 -37 -35 40 -91
65 -61 27 0 61 46
-95 -2 84 -67 -58 -77 95
6 62 34 -86 -76 -80 -54
52 -12 -28 -46 46 -91
-67 94 -38 98 -68 3 -28 57 -77 38
54 29 31 10 77 -10 64
96 34 -43
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2
4
5
3
2
3
4
4
3
2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
21 -29 -86 -47 82 -51
-40 -48
23 63 -90 -41 -65
11 87 -2 -61 71 -67 -97 -95 -5
29 82 -62 80 33 -35
-96 -10 34 -70 33 -33 -52 84 71
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
3
1
2
4
3
4
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-85 -5 22 13 69 60 68 27
-74 90 33 16 36
73 28 26 -91 -40
25 28 -94 87 55 18
25 61 52 71 -30 58 86 39 77
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
3
2
3
3
3
```
