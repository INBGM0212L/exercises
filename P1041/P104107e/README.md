# `P104107e` - Nemnegatív elemek száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_non_negatives` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi nemnegatív!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[50, 98, -95, 38, 44, -21, -5, -25]` | `4` |
 | `[12, 25, -12]` | `2` |
 | `[-85]` | `0` |
 | `[9, 77, -18, -57, -5, 59, 71, 14, 35, 14]` | `7` |
 | `[41, 2, -64, -27]` | `2` |
 | `[82, 71, 16, -70, 32, 73, 21, -8]` | `6` |
 | `[29, 57]` | `2` |
 | `[61, 83, -95, -74, 58, -73, -34, 63, -39, 11]` | `5` |
 | `[-54, 24, -93, 92, 88, -43, 9, 77, 65]` | `6` |
 | `[-6, 13, 20]` | `2` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
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
50 98 -95 38 44 -21 -5 -25
12 25 -12
-85
9 77 -18 -57 -5 59 71 14 35 14
41 2 -64 -27
82 71 16 -70 32 73 21 -8
29 57
61 83 -95 -74 58 -73 -34 63 -39 11
-54 24 -93 92 88 -43 9 77 65
-6 13 20
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
4
2
0
7
2
6
2
5
6
2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-21 43 8 28 89
-7 -2
10 91
-38
-82 16 48 -86 78 64 77
5 59 66 14 -62 20
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
4
0
2
0
5
5
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8 95
49
48
-27 -91 47 -71 -30 80 -72 94 22 -55
84 -63 -77 -25 -39 21 -79
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
2
1
1
4
2
```
