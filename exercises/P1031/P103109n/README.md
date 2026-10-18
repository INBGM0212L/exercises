# `P103109n` - Négyzet kerülete v2 (`n` teszteset)

## A függvény
Írj egy `square_circumference_v2` nevű függvényt, mely visszaadja a paraméterként megkapott oldalhosszúságú négyzet kerületét a `rectangle_circumference()` függvény felhasználásával!


### Paraméterlista
1. `n` - a négyzet oldalhossza (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a négyzet kerülete

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `99` | `396` |
 | `25` | `100` |
 | `11` | `44` |
 | `83` | `332` |
 | `14` | `56` |
 | `29` | `116` |
 | `82` | `328` |
 | `25` | `100` |
 | `41` | `164` |
 | `69` | `276` |


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
10
99
25
11
83
14
29
82
25
41
69
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
396
100
44
332
56
116
328
100
164
276
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5
34
29
93
10
29
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
136
116
372
40
116
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
7
13
80
4
8
14
59
51
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
52
320
16
32
56
236
204
```
