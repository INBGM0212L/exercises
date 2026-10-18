# `P104106e` - Negatív elemek száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_negatives` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi negatív!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[-27, 7, -35, 71, 83, 11, 31, 60, 99, 65]` | `2` |
 | `[51, 32, 72, 42]` | `0` |
 | `[23, -4, -43, 29, 50, 55, 76]` | `2` |
 | `[-11, 67, -21]` | `2` |
 | `[-13, -53, 89]` | `2` |


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
-27 7 -35 71 83 11 31 60 99 65
51 32 72 42
23 -4 -43 29 50 55 76
-11 67 -21
-13 -53 89
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2
0
2
2
2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-83 5 17 -79 64 74 -48 -41 14
1 -8 87 -55 -9 -63 11 37 -16
45 10 86
-39 79 -33 -66 -41 42 14 2 98
-26
-16 -20 -13 9
-35 -40 48 52 13 -92 96 27 48
74 -36 0 -51 -64 -31 -22 69 -56
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
4
5
0
4
1
3
3
6
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
17 47
-82 28 83 83 -14 -84 -8 -96 59 65
-69
2 -35 96 -77 -24
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
0
5
1
3
```
