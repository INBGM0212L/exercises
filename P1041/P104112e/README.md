# `P104112e` - Nemnövekvő szomszédok száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_non_increasing_neighbours` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott listában hány olyan elem van, mely nem nagyobb az őt megelőzőnél!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[-63, 64, 42, -79, 66, -40, 71, 30, 60, -11]` | `5` |
 | `[-70, -17, 0, 13]` | `0` |
 | `[-44, -19, -68]` | `1` |
 | `[-34, -10, 66, -29, 92, 52, -17, -51, -89, 30]` | `5` |
 | `[-56, 82, -12]` | `1` |
 | `[22, -27, 16, -56, 34, 13, -97, -64, 80]` | `4` |


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
-63 64 42 -79 66 -40 71 30 60 -11
-70 -17 0 13
-44 -19 -68
-34 -10 66 -29 92 52 -17 -51 -89 30
-56 82 -12
22 -27 16 -56 34 13 -97 -64 80
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
5
0
1
5
1
4
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
70
-21
22 -67 -38
96 -3 67 7 23
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
0
0
1
2
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-12
34 -43 -47 12 -46 -67
-17 98 -56
97 19 -15 39 -13
-98 -17 -76 96 -4
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
0
4
1
3
2
```
