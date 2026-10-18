# `P103209n` - Euklideszi távolság kerekítve (`n` teszteset)

## A függvény
Írj egy `euclidean_distance_rounded` nevű függvényt, mely visszaadja a paraméterként megkapott két pont (`(x1, y1)` és `(x2, y2)`) `d` tizedesjegy pontosságúra kerekített euklideszi távolságát!


### Paraméterlista
1. `x1` - az első pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
2. `y1` - az első pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)
3. `x2` - a második pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
4. `y2` - a második pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)
5. `d` - a kerekítés `d` pontossága (egész érték a(z) `[1,6]` intervallumból)

### Visszaadott érték
* a két pont kerekített euklideszi távolsága

### Példák
 | `x1` | `y1` | `x2` | `y2` | `d` | Visszaadott érték |
 | :--- | :--- | :--- | :--- | :--- | :-- |
 | `26.66` | `7.96` | `72.76` | `7.14` | `6` | `46.107292` |
 | `47.01` | `42.68` | `16.73` | `12.81` | `5` | `42.53346` |
 | `79.84` | `8.92` | `5.73` | `21.32` | `1` | `75.1` |
 | `40.99` | `65.91` | `63.53` | `55.27` | `1` | `24.9` |
 | `48.33` | `10.14` | `26.32` | `63.57` | `4` | `57.7859` |
 | `95.11` | `57.68` | `23.43` | `56.68` | `6` | `71.686975` |
 | `81.07` | `27.22` | `77.16` | `78.07` | `4` | `51.0001` |
 | `29.75` | `20.98` | `72.89` | `7.07` | `6` | `45.327119` |
 | `6.83` | `40.09` | `69.22` | `96.66` | `3` | `84.218` |


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
9
26.66 7.96 72.76 7.14 6
47.01 42.68 16.73 12.81 5
79.84 8.92 5.73 21.32 1
40.99 65.91 63.53 55.27 1
48.33 10.14 26.32 63.57 4
95.11 57.68 23.43 56.68 6
81.07 27.22 77.16 78.07 4
29.75 20.98 72.89 7.07 6
6.83 40.09 69.22 96.66 3
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
46.107292
42.53346
75.1
24.9
57.7859
71.686975
51.0001
45.327119
84.218
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
4
85.42 49.38 10.91 53.28 6
41.55 6.91 21.74 47.46 2
21.32 63.68 28.28 59.42 3
26.78 14.14 63.74 8.88 2
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
74.611997
45.13
8.16
37.33
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
9
95.06 18.2 87.03 76.57 3
92.81 37.46 71.75 30.23 4
80.48 39.48 76.51 36.04 5
93.67 94.71 53.99 73.78 5
74.71 67.11 41.33 94.13 1
43.52 2.87 46.58 9.29 1
24.35 39.08 96.17 73.63 5
45.83 53.64 96.03 8.02 4
28.42 73.99 79.18 86.47 1
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
58.92
22.2665
5.25305
44.86165
42.9
7.1
79.69827
67.8323
52.3
```
