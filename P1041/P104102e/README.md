# `P104102e` - Páros elemek száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_evens` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi páros szám!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[70, -64]` | `2` |
 | `[-51, 61, 48, -19, 64, -69, -99, -39]` | `2` |
 | `[77, 95, -11, 87, 53, -38, 9, 24]` | `2` |


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
70 -64
-51 61 48 -19 64 -69 -99 -39
77 95 -11 87 53 -38 9 24
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2
2
2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
20 -73 -53 68 29 84 65 48 80 -84
-98 75 -41 95 -91 -83 53 -72
55 -63 -90 -22 -43 94 -38
23 -87 61 -45 -94 35 -5 31
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
6
2
4
1
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-9 62 44
63
-71 -75 -69 83 1
-73 -43 56 90 -10 26 43 -91
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
2
0
0
4
```
