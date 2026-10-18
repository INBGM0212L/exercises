# `P103208t` - Euklideszi távolság (végjelig olvasás)

## A függvény
Írj egy `euclidean_distance` nevű függvényt, mely visszaadja a paraméterként megkapott két pont (`(x1, y1)` és `(x2, y2)` euklideszi távolságát!


### Paraméterlista
1. `x1` - az első pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
2. `y1` - az első pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)
3. `x2` - a második pont `x` koordinátája (valós érték a(z) `[1,100]` intervallumból)
4. `y2` - a második pont `y` koordinátája (valós érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a két pont euklideszi távolsága

### Példák
 | `x1` | `y1` | `x2` | `y2` | Visszaadott érték |
 | :--- | :--- | :--- | :--- | :-- |
 | `79.38` | `94.8` | `30.86` | `28.27` | `82.34337435398187` |
 | `94.55` | `22.6` | `88.96` | `79.0` | `56.67634515386468` |
 | `37.95` | `67.56` | `72.18` | `47.06` | `39.899159139009434` |
 | `99.65` | `28.11` | `53.22` | `54.2` | `53.25817308169706` |
 | `14.3` | `29.71` | `73.28` | `99.5` | `91.37441928680039` |
 | `78.95` | `46.89` | `67.39` | `20.72` | `28.60948269368043` |
 | `84.78` | `20.13` | `97.9` | `43.22` | `26.55715534465241` |
 | `20.68` | `67.02` | `91.93` | `81.42` | `72.69059430215164` |
 | `11.67` | `59.0` | `33.91` | `2.0` | `61.18510929956732` |
 | `71.57` | `45.67` | `61.59` | `9.99` | `37.04946423364311` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`
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
79.38 94.8 30.86 28.27
94.55 22.6 88.96 79.0
37.95 67.56 72.18 47.06
99.65 28.11 53.22 54.2
14.3 29.71 73.28 99.5
78.95 46.89 67.39 20.72
84.78 20.13 97.9 43.22
20.68 67.02 91.93 81.42
11.67 59.0 33.91 2.0
71.57 45.67 61.59 9.99
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
82.34337435398187
56.67634515386468
39.899159139009434
53.25817308169706
91.37441928680039
28.60948269368043
26.55715534465241
72.69059430215164
61.18510929956732
37.04946423364311
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
30.89 59.64 20.05 35.05
45.38 35.51 96.36 73.45
75.71 87.07 36.84 52.39
79.64 84.64 94.42 61.38
64.61 38.21 81.09 82.47
22.5 70.56 21.38 72.26
90.03 38.41 32.45 98.3
14.22 92.43 21.92 7.4
52.6 64.9 71.8 94.07
10.14 22.98 87.41 57.29
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
26.87328971302174
63.54843821841729
52.09202722106329
27.558592126594565
47.228571860686195
2.0357799488156894
83.07989227243858
85.37792981795705
34.921753965114625
84.54483425969916
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
39.79 90.82 24.98 60.69
55.36 21.09 14.96 86.1
48.67 4.55 60.6 92.45
38.53 90.59 93.94 17.38
56.32 74.11 8.68 53.23
74.49 75.59 34.83 43.29
38.15 12.45 48.39 67.63
97.83 14.35 34.15 21.35
35.06 91.29 8.79 46.68
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
33.57309935052169
76.54057812689945
88.70588988336682
91.81488005764643
52.014844035140584
51.14885726973771
56.12209903415944
64.06358091771018
51.77031002418279
```
