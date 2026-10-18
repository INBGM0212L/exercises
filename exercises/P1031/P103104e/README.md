# `P103104e` - Négyzet területe (állományvégjelig olvasás)

## A függvény
Írj egy `square_area` nevű függvényt, mely visszaadja a paraméterként megkapott oldalhosszúságú négyzet területét!


### Paraméterlista
1. `n` - a négyzet oldalhossza (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a négyzet területe

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `22` | `484` |
 | `84` | `7056` |
 | `86` | `7396` |
 | `91` | `8281` |
 | `62` | `3844` |
 | `93` | `8649` |
 | `6` | `36` |
 | `13` | `169` |
 | `51` | `2601` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`n`) szerepel.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
22
84
86
91
62
93
6
13
51
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
484
7056
7396
8281
3844
8649
36
169
2601
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
89
100
52
85
8
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
7921
10000
2704
7225
64
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
24
100
37
40
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
576
10000
1369
1600
```
