# `P104304e` - Lista modulo művelete (állományvégjelig olvasás)

## A függvény
Írj egy `apply_modulo` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemére elvégezzük az `element mod divisor` műveletet!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)
2. `divisor` - az osztó tényező (egész érték a(z) `[1,20]` intervallumból)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | `divisor` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `[-9, -59, -16]` | `9` | `[0, 4, 2]` |
 | `[62, -8, 20, -5, -19]` | `10` | `[2, 2, 0, 5, 1]` |
 | `[-2, 12]` | `15` | `[13, 12]` |
 | `[85, 7, 54, -62, 47, -49, 81, 77]` | `6` | `[1, 1, 0, 4, 5, 5, 3, 5]` |


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
-9 -59 -16
9
62 -8 20 -5 -19
10
-2 12
15
85 7 54 -62 47 -49 81 77
6
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
0 4 2
2 2 0 5 1
13 12
1 1 0 4 5 5 3 5
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
85 95 -69 0 -67 78 71 -88 32 -80
15
-46 -85 67 -35 96 -74
2
-42
11
29 34 24 86 73 94 -3 -36
17
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
10 5 6 0 8 3 11 2 2 10
0 1 1 1 0 0
2
12 0 7 1 5 9 14 15
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-6 61 -73
13
-63 72 52 40 84 -7 16 5 31
5
-5 -24 -9 -77 -57 70 -40 19
15
95 33 -57
5
31 -92 78 84 -52 -69 -12
15
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
7 9 5
2 2 2 0 4 3 1 0 1
10 6 6 13 3 10 5 4
0 3 3
1 13 3 9 8 6 3
```
