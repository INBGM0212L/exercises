# `P104302e` - Lista egész osztása (állományvégjelig olvasás)

## A függvény
Írj egy `apply_integer_division` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemét elosztjuk a `divisor` paraméter értékkel!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)
2. `divisor` - az osztó tényező (egész érték a(z) `[-100,100]` intervallumból)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | `divisor` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `[52, -33, 11, 46, -63, -65, -85, -29]` | `24` | `[2, -2, 0, 1, -3, -3, -4, -2]` |
 | `[-57, 45, 55, -10, 11, 44, 23]` | `9` | `[-7, 5, 6, -2, 1, 4, 2]` |
 | `[98, -11, -36, 79, 5, 94, 45]` | `71` | `[1, -1, -1, 1, 0, 1, 0]` |
 | `[69, 16, -71, 61, -31, -90, 1]` | `-22` | `[-4, -1, 3, -3, 1, 4, -1]` |
 | `[-5, -45, 72, 86]` | `51` | `[-1, -1, 1, 1]` |
 | `[-39]` | `3` | `[-13]` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy harmadik, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza. A tömb végét egy extra, `INT_MIN` értékű elem jelzi.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
52 -33 11 46 -63 -65 -85 -29
24
-57 45 55 -10 11 44 23
9
98 -11 -36 79 5 94 45
71
69 16 -71 61 -31 -90 1
-22
-5 -45 72 86
51
-39
3
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2 -2 0 1 -3 -3 -4 -2
-7 5 6 -2 1 4 2
1 -1 -1 1 0 1 0
-4 -1 3 -3 1 4 -1
-1 -1 1 1
-13
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-70 -67 -20 41 75 90
-35
86 32 28 -62 -6 47
-41
17 68 -20 -89
-12
-90 -97 -51 48 -85 50 -13 -44 -34 -66
-20
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
2 1 0 -2 -3 -3
-3 -1 -1 1 0 -2
-2 -6 1 7
4 4 2 -3 4 -3 0 2 1 3
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
57 -28 65 47 97 32 2
-28
75 50 16 75 -83 67 -82
49
-7 73 36
-77
23 -94 48 -36 -91 -6
-80
77 14 -29 -80 -38
67
88 32 -23 10 44 80
-88
-49 21 76 63 -84 95 75 76 2
40
83 -87 -89
-66
-36
-94
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
-3 1 -3 -2 -4 -2 -1
1 1 0 1 -2 1 -2
0 -1 -1
-1 1 -1 0 1 0
1 0 -1 -2 -1
-1 -1 0 -1 -1 -1
-2 0 1 1 -3 2 1 1 0
-2 1 1
0
```
