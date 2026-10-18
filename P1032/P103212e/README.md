# `P103212e` - Pitagorasz tétel (állományvégjelig olvasás)

## A függvény
Írj egy `pythagorean` nevű függvényt, mely visszaadja a két befogó (`a` és `b`) ismeretében egy háromszög átfogóját!


### Paraméterlista
1. `a` - az `a` befogó hossza (valós érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` befogó hossza (valós érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* az átfogó hossza

### Példák
 | `a` | `b` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `86.3` | `50.47` | `99.97455126180861` |
 | `59.73` | `39.11` | `71.39513288733343` |
 | `57.4` | `55.74` | `80.01067178820585` |
 | `61.91` | `52.71` | `81.30923809752493` |
 | `11.15` | `87.08` | `87.79093859846812` |
 | `96.02` | `56.16` | `111.23752064838554` |
 | `18.11` | `71.23` | `73.49615636208468` |
 | `62.48` | `64.02` | `89.45563593200822` |
 | `51.66` | `53.15` | `74.11935037491895` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`a` és `b`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
86.3 50.47
59.73 39.11
57.4 55.74
61.91 52.71
11.15 87.08
96.02 56.16
18.11 71.23
62.48 64.02
51.66 53.15
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
99.97455126180861
71.39513288733343
80.01067178820585
81.30923809752493
87.79093859846812
111.23752064838554
73.49615636208468
89.45563593200822
74.11935037491895
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
22.73 69.52
27.0 31.09
65.53 33.95
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
73.14152924296839
41.17751935219022
73.80232652159415
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
57.11 8.04
94.9 70.15
25.52 53.47
42.38 45.33
58.53 6.96
4.35 31.79
59.65 98.62
30.96 3.27
90.62 30.51
61.87 75.78
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
57.67316273623287
118.0128488767219
59.24788013085362
62.05540508287735
58.94236591790323
32.08623692488728
115.25635297023761
31.132210008285632
95.61822263564619
97.82895941386681
```
