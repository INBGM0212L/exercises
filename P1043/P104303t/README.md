# `P104303t` - Lista valós osztása (végjelig olvasás)

## A függvény
Írj egy `apply_float_division` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemét elosztjuk a `divisor` paraméter értékkel, majd `3` tizedesjegyre kerekítünk!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)
2. `divisor` - az osztó tényező (egész érték a(z) `[-100,100]` intervallumból)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | `divisor` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `[60]` | `-6` | `[-10.0]` |
 | `[40, 21, 88]` | `-71` | `[-0.563, -0.296, -1.239]` |
 | `[88, -46, -39, 50, 69, 3, -84, -17, 2]` | `-10` | `[-8.8, 4.6, 3.9, -5.0, -6.9, -0.3, 8.4, 1.7, -0.2]` |
 | `[79, 51, 98, -12, -4]` | `-69` | `[-1.145, -0.739, -1.42, 0.174, 0.058]` |
 | `[46, 43, -59, -82]` | `-64` | `[-0.719, -0.672, 0.922, 1.281]` |
 | `[66, 63]` | `-65` | `[-1.015, -0.969]` |
 | `[-23, 90, 47]` | `16` | `[-1.438, 5.625, 2.938]` |
 | `[-72, -90, -40, -22, -49, -90]` | `-73` | `[0.986, 1.233, 0.548, 0.301, 0.671, 1.233]` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy harmadik, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza. A tömb végét egy extra, `INT_MIN` értékű elem jelzi.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.
* A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. Lehetséges hogy a két nyelv kerekítési hibája nem pontosan ugyanaz valós értékeknél.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
60
-6
40 21 88
-71
88 -46 -39 50 69 3 -84 -17 2
-10
79 51 98 -12 -4
-69
46 43 -59 -82
-64
66 63
-65
-23 90 47
16
-72 -90 -40 -22 -49 -90
-73
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
-10.0
-0.563 -0.296 -1.239
-8.8 4.6 3.9 -5.0 -6.9 -0.3 8.4 1.7 -0.2
-1.145 -0.739 -1.42 0.174 0.058
-0.719 -0.672 0.922 1.281
-1.015 -0.969
-1.438 5.625 2.938
0.986 1.233 0.548 0.301 0.671 1.233
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-43 90 50
23
12 9 41 70 -10 65 80
-1
-69 -53 49
-34
75
8
-65 -24 94 96
-96
-81 45 -54 75 -56 85 -74 15
-28
51 26 -69 55 -73 -80 -26 -44 57
54
76 -45 41 29 -62 8 98
64
-11 69 12 -27 -94 30 -19 9 -89 -49
-40
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
-1.87 3.913 2.174
-12.0 -9.0 -41.0 -70.0 10.0 -65.0 -80.0
2.029 1.559 -1.441
9.375
0.677 0.25 -0.979 -1.0
2.893 -1.607 1.929 -2.679 2.0 -3.036 2.643 -0.536
0.944 0.481 -1.278 1.019 -1.352 -1.481 -0.481 -0.815 1.056
1.188 -0.703 0.641 0.453 -0.969 0.125 1.531
0.275 -1.725 -0.3 0.675 2.35 -0.75 0.475 -0.225 2.225 1.225
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
30 -4 30 -88 -56 -6 -66 -98
93
-46
-62
-74 47 -30 -19 58 31
85
-75 -97 97 -83 -83 -61 68 33 -82
-19
34
-12
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
0.323 -0.043 0.323 -0.946 -0.602 -0.065 -0.71 -1.054
0.742
-0.871 0.553 -0.353 -0.224 0.682 0.365
3.947 5.105 -5.105 4.368 4.368 3.211 -3.579 -1.737 4.316
-2.833
```
