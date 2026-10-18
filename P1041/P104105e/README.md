# `P104105e` - Pozitív elemek száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_positives` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi pozitív!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[82, 96, 88, 21, -25, 59, 49, -9]` | `6` |
 | `[-6, 95, -47, -5]` | `1` |
 | `[15, -31, -40, 33, 71, -15, -13, 28, -22, -52]` | `4` |
 | `[0, -70, 30, 48, -9, -8]` | `2` |
 | `[15, 11, -40, -41]` | `2` |
 | `[-38, 99, -2, 89, -31]` | `2` |


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
82 96 88 21 -25 59 49 -9
-6 95 -47 -5
15 -31 -40 33 71 -15 -13 28 -22 -52
0 -70 30 48 -9 -8
15 11 -40 -41
-38 99 -2 89 -31
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
6
1
4
2
2
2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
39 -9 98 51 -78
-80
-52
-49 -56 15 -36
-41 98 38 42 6 7 -22 -36
-96 -36
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
3
0
0
1
5
0
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
74 -29 -87 63
22 -3 -75 28 65 -63 42 -39 9
49 -40 70 32 -59 1 20
51
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
2
5
5
1
```
