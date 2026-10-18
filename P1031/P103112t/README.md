# `P103112t` - Kör kerekített területe (végjelig olvasás)

## A függvény
Írj egy `circle_area_rounded` nevű függvényt, mely visszaadja a paraméterként megkapott `r` sugarú kör területét `d` tizedesjegyre kerekítve!


### Paraméterlista
1. `r` - a kör sugara (egész érték a(z) `[1,100]` intervallumból)
2. `d` - a kerekítés pontossága (egész érték a(z) `[0,7]` intervallumból)

### Visszaadott érték
* a kör kerekített területe

### Példák
 | `r` | `d` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `34` | `4` | `3631.6811` |
 | `9` | `3` | `254.469` |
 | `55` | `3` | `9503.318` |
 | `39` | `1` | `4778.4` |
 | `87` | `5` | `23778.7148` |
 | `98` | `0` | `30172.0` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`r` és `d`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
34 4
9 3
55 3
39 1
87 5
98 0
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
3631.6811
254.469
9503.318
4778.4
23778.7148
30172.0
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
11 4
92 0
65 2
51 0
33 1
75 3
52 3
10 4
42 0
58 5
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
380.1327
26590.0
13273.23
8171.0
3421.2
17671.459
8494.867
314.1593
5542.0
10568.31769
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
76 1
55 6
49 2
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
18145.8
9503.317777
7542.96
```
