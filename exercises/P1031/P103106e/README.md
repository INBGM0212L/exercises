# `P103106e` - Téglalap területe (állományvégjelig olvasás)

## A függvény
Írj egy `rectangle_area` nevű függvényt, mely visszaadja a paraméterként megkapott oldalhosszúságú téglalap területét!


### Paraméterlista
1. `a` - az `a` oldal hossza (egész érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` oldal hossza (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a téglalap területe

### Példák
 | `a` | `b` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `25` | `1` | `25` |
 | `55` | `34` | `1870` |
 | `12` | `37` | `444` |
 | `2` | `57` | `114` |
 | `49` | `46` | `2254` |
 | `61` | `8` | `488` |
 | `7` | `34` | `238` |
 | `8` | `85` | `680` |
 | `50` | `85` | `4250` |
 | `34` | `65` | `2210` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`a` és `b`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
25 1
55 34
12 37
2 57
49 46
61 8
7 34
8 85
50 85
34 65
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
25
1870
444
114
2254
488
238
680
4250
2210
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
62 73
59 3
24 80
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
4526
177
1920
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
85 4
58 21
23 20
28 71
52 29
82 96
57 30
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
340
1218
460
1988
1508
7872
1710
```
