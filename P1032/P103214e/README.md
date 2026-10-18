# `P103214e` - Számtani sorozat `n`. eleme (állományvégjelig olvasás)

## A függvény
Írj egy `arithmetic_sequence_element` nevű függvényt, mely visszaadja az (`a`, `d`) paraméterű számtani sorozat `n`. elemét!


### Paraméterlista
1. `a` - a sorozat első eleme (egész érték a(z) `[1,100]` intervallumból)
2. `n` - az `n` értéke (egész érték a(z) `[1,100]` intervallumból)
3. `d` - a sorozat differenciája (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a sorozat `n`. eleme

### Példák
 | `a` | `n` | `d` | Visszaadott érték |
 | :--- | :--- | :--- | :-- |
 | `41` | `6` | `87` | `476` |
 | `25` | `49` | `65` | `3145` |
 | `23` | `90` | `70` | `6253` |
 | `57` | `55` | `66` | `3621` |
 | `70` | `4` | `2` | `76` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`a`, `n` és `d`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
41 6 87
25 49 65
23 90 70
57 55 66
70 4 2
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
476
3145
6253
3621
76
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
34 92 63
60 76 19
78 62 5
14 14 95
60 49 14
59 4 67
10 40 3
45 95 85
93 72 13
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
5767
1485
383
1249
732
260
127
8035
1016
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
68 13 18
4 23 61
60 55 40
13 50 20
95 17 22
91 3 12
74 64 100
8 32 19
68 46 59
3 24 88
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
284
1346
2220
993
447
115
6374
597
2723
2027
```
