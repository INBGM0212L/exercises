# `P103213n` - Pitagorasz tétel kerekítve (`n` teszteset)

## A függvény
Írj egy `pythagorean_rounded` nevű függvényt, mely visszaadja a két befogó (`a` és `b`) ismeretében egy háromszög átfogójának `d` tizedesjegyre kerekített hosszát!


### Paraméterlista
1. `a` - az `a` befogó hossza (valós érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` befogó hossza (valós érték a(z) `[1,100]` intervallumból)
3. `d` - a kerekítés `d` pontossága (egész érték a(z) `[1,6]` intervallumból)

### Visszaadott érték
* az átfogó kerített hossza

### Példák
 | `a` | `b` | `d` | Visszaadott érték |
 | :--- | :--- | :--- | :-- |
 | `28.53` | `9.06` | `3` | `29.934` |
 | `97.85` | `57.31` | `5` | `113.39779` |
 | `64.67` | `81.35` | `6` | `103.9232` |
 | `90.14` | `54.41` | `1` | `105.3` |
 | `39.14` | `90.8` | `2` | `98.88` |
 | `44.64` | `8.41` | `6` | `45.425298` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`a`, `b` és `d`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
6
28.53 9.06 3
97.85 57.31 5
64.67 81.35 6
90.14 54.41 1
39.14 90.8 2
44.64 8.41 6
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
29.934
113.39779
103.9232
105.3
98.88
45.425298
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
9
93.7 13.24 6
56.94 14.16 5
76.99 39.45 1
34.39 15.43 1
85.56 96.7 5
92.24 3.0 5
95.69 8.79 1
66.54 94.74 6
15.23 69.35 2
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
94.630796
58.67426
86.5
37.7
129.11779
92.28877
96.1
115.772359
71.0
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
5
39.57 62.66 2
80.36 1.07 1
30.15 55.64 2
75.7 77.49 1
10.92 34.55 2
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
74.11
80.4
63.28
108.3
36.23
```
