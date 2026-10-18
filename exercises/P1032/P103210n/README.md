# `P103210n` - Manhattan távolság (`n` teszteset)

## A függvény
Írj egy `manhattan_distance` nevű függvényt, mely visszaadja a paraméterként megkapott két pont (`(x1, y1)` és `(x2, y2)`) Manhattan távolságát!


### Paraméterlista
1. `x1` - az első pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
2. `y1` - az első pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)
3. `x2` - a második pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
4. `y2` - a második pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a két pont Manhattan távolsága

### Példák
 | `x1` | `y1` | `x2` | `y2` | Visszaadott érték |
 | :--- | :--- | :--- | :--- | :-- |
 | `23.74` | `27.66` | `9.27` | `76.59` | `63.400000000000006` |
 | `94.8` | `94.5` | `20.23` | `93.34` | `75.72999999999999` |
 | `51.87` | `62.1` | `98.19` | `98.91` | `83.13` |
 | `70.7` | `4.76` | `86.66` | `47.97` | `59.169999999999995` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`x1`, `y1`, `x2` és `y2`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

## Megjegyzés a *C* nyelvű megoldásokhoz
A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. Lehetséges hogy a két nyelv kerekítési hibája nem pontosan ugyanaz valós értékeknél.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
4
23.74 27.66 9.27 76.59
94.8 94.5 20.23 93.34
51.87 62.1 98.19 98.91
70.7 4.76 86.66 47.97
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
63.400000000000006
75.72999999999999
83.13
59.169999999999995
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
9
82.39 99.37 73.23 62.19
50.03 5.42 95.3 28.61
52.66 26.15 31.7 44.02
58.67 65.89 30.35 27.55
95.34 94.66 41.92 32.41
92.91 73.6 23.09 39.3
50.07 77.05 4.58 82.79
90.37 4.52 98.65 70.41
32.52 22.21 94.73 57.67
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
46.34
68.46
38.83
66.66
115.67
104.11999999999999
51.23000000000001
74.17
97.67
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
9
68.6 82.36 11.14 92.66
68.15 2.47 93.5 90.63
67.26 14.39 83.28 47.69
62.74 50.7 88.12 85.83
78.71 30.81 67.59 56.43
49.99 63.07 32.46 47.47
23.9 23.27 61.72 45.03
27.0 28.85 90.42 18.06
80.5 96.67 41.41 38.19
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
67.75999999999999
113.50999999999999
49.31999999999999
60.51
36.739999999999995
33.13
59.58
74.21000000000001
97.57000000000001
```
