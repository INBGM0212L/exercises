# `P103211n` - Manhattan távolság kerekítve (`n` teszteset)

## A függvény
Írj egy `manhattan_distance_rounded` nevű függvényt, mely visszaadja a paraméterként megkapott két pont (`(x1, y1)` és `(x2, y2)`) `d` tizedesjegy pontosságúra kerekített Manhattan távolságát!


### Paraméterlista
1. `x1` - az első pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
2. `y1` - az első pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)
3. `x2` - a második pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
4. `y2` - a második pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)
5. `d` - a kerekítés `d` pontossága (egész érték a(z) `[1,6]` intervallumból)

### Visszaadott érték
* a két pont kerekített Manhattan távolsága

### Példák
 | `x1` | `y1` | `x2` | `y2` | `d` | Visszaadott érték |
 | :--- | :--- | :--- | :--- | :--- | :-- |
 | `88.59` | `38.31` | `55.07` | `27.01` | `2` | `44.82` |
 | `20.63` | `64.68` | `67.95` | `67.31` | `4` | `49.95` |
 | `55.43` | `39.35` | `81.13` | `18.6` | `2` | `46.45` |
 | `46.58` | `53.99` | `29.58` | `72.13` | `5` | `35.14` |
 | `26.05` | `41.82` | `93.49` | `94.01` | `1` | `119.6` |
 | `46.7` | `4.99` | `2.13` | `59.07` | `1` | `98.7` |
 | `56.6` | `20.77` | `26.15` | `93.71` | `1` | `103.4` |
 | `88.76` | `49.54` | `45.56` | `80.69` | `1` | `74.3` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`x1`, `y1`, `x2`, `y2` és `d`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
8
88.59 38.31 55.07 27.01 2
20.63 64.68 67.95 67.31 4
55.43 39.35 81.13 18.6 2
46.58 53.99 29.58 72.13 5
26.05 41.82 93.49 94.01 1
46.7 4.99 2.13 59.07 1
56.6 20.77 26.15 93.71 1
88.76 49.54 45.56 80.69 1
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
44.82
49.95
46.45
35.14
119.6
98.7
103.4
74.3
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
8
49.96 42.26 18.9 31.06 2
73.76 77.59 19.81 80.83 4
92.54 90.55 47.6 38.77 2
68.48 85.09 32.77 36.94 3
65.88 97.85 44.92 52.87 4
52.53 72.88 96.22 47.35 2
55.98 49.01 60.97 13.31 2
73.83 95.45 67.44 43.84 3
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
42.26
57.19
96.72
83.86
65.94
69.22
40.69
58.0
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8
36.02 86.58 99.88 84.08 3
97.52 36.73 69.02 27.17 5
2.58 34.48 70.58 92.54 4
23.2 28.85 21.22 3.27 1
24.71 19.03 87.32 62.12 1
29.59 13.06 27.6 76.65 3
2.57 90.09 1.27 11.19 2
33.48 67.41 89.82 83.69 5
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
66.36
38.06
126.06
27.6
105.7
65.58
80.2
72.62
```
