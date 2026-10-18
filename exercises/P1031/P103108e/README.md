# `P103108e` - Négyzet területe v2 (állományvégjelig olvasás)

## A függvény
Írj egy `square_area_v2` nevű függvényt, mely visszaadja a paraméterként megkapott oldalhosszúságú négyzet területét a `rectangle_area()` függvény felhasználásával!


### Paraméterlista
1. `n` - a négyzet oldalhossza (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a négyzet területe

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `66` | `4356` |
 | `76` | `5776` |
 | `21` | `441` |
 | `89` | `7921` |
 | `19` | `361` |
 | `45` | `2025` |
 | `73` | `5329` |
 | `9` | `81` |
 | `71` | `5041` |
 | `48` | `2304` |


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
66
76
21
89
19
45
73
9
71
48
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
4356
5776
441
7921
361
2025
5329
81
5041
2304
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
92
88
52
35
59
82
37
19
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
8464
7744
2704
1225
3481
6724
1369
361
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
66
54
72
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
4356
2916
5184
```
