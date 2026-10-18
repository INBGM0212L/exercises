# `P104108t` - Lokális minimumhelyek száma (végjelig olvasás)

## A függvény
Írj egy `count_of_local_minimums` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott listában hány elem kisebb mindkét szomszédjánál!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[97, -52, -12, 41, 87, 19, 35, -45, 43]` | `3` |
 | `[18, 92, -21, -86, 65]` | `1` |
 | `[-60, -5, -73, -96, -31, 1, 72]` | `1` |
 | `[-42, 2, -67, -1, -35, 46, 32, -46, 71, -56]` | `3` |
 | `[-65, -63, 3, -60, -14, 61, 41, -53]` | `1` |
 | `[-60, 84, 47, -76, -68, 4]` | `1` |
 | `[-22, 18, -80, -99, 76, -5]` | `1` |
 | `[-6, -22, 29, -24, 58, 44, 99, -67]` | `3` |
 | `[8, 8, -43, -85, 30, 84]` | `1` |


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
97 -52 -12 41 87 19 35 -45 43
18 92 -21 -86 65
-60 -5 -73 -96 -31 1 72
-42 2 -67 -1 -35 46 32 -46 71 -56
-65 -63 3 -60 -14 61 41 -53
-60 84 47 -76 -68 4
-22 18 -80 -99 76 -5
-6 -22 29 -24 58 44 99 -67
8 8 -43 -85 30 84
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
3
1
1
3
1
1
1
3
1
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
33 82 8 -99 40
-64 20 40 94 -59 -77 -85 36
96 -58 4 76 -43 -37 -60
42 81 -91
19 -52 -6 15
-94
-73 14
-92 91 -22 -99 -91 88 -87 66
44 -36 -59 64 -61 -53 -7
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
1
1
2
0
1
0
0
2
2
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
76 -15 -43 98 63 1 46 -17 6
-73 -71
-48 -28 59 -34 63 -31 -78 -73
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
3
0
2
```
