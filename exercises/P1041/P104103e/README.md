# `P104103e` - Prím elemek száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_primes` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi prímszám!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `1`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[92, 53, 25, 4, 83, 41]` | `3` |
 | `[68, 9, 59, 15, 39, 55, 45, 17]` | `2` |
 | `[79, 12, 65, 39, 32, 12, 68, 82, 24, 42]` | `1` |
 | `[31, 81, 97]` | `2` |
 | `[17, 49]` | `1` |
 | `[41, 79, 38, 99, 84, 60, 25]` | `2` |


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
92 53 25 4 83 41
68 9 59 15 39 55 45 17
79 12 65 39 32 12 68 82 24 42
31 81 97
17 49
41 79 38 99 84 60 25
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
3
2
1
2
1
2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
82 6 86 61 87 68
50 53 29 79 30 6 57 77 2 24
32 78
20 59 16 17
13 17 43 48 47 26 40 40 66 12
57 94 81 61 28 65 97 83 68 77
18 91 25 63 66 82 52 7 43 6
80 98
50 66
75 97 54 77 51 32 3
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
1
4
0
2
4
3
2
0
0
2
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
55 79 34 90
18 97
37 6 62 86
23 41 13 37 90 14 34
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
1
1
1
4
```
