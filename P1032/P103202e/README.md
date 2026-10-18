# `P103202e` - Legkisebb közös többszörös (állományvégjelig olvasás)

## A függvény
Írj egy `lcm` nevű függvényt, mely visszaadja a paraméterként megkapott két szám (`a` és `b`) legkisebb közös többszörösét!


### Paraméterlista
1. `a` - az `a` értéke (egész érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` értéke (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a legkisebb közös többszörös

### Példák
 | `a` | `b` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `82` | `33` | `2706` |
 | `9` | `30` | `90` |
 | `68` | `54` | `1836` |
 | `10` | `13` | `130` |


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
82 33
9 30
68 54
10 13
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2706
90
1836
130
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
21 21
25 57
32 86
69 35
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
21
1425
1376
2415
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
96 46
65 83
51 75
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
2208
5395
1275
```
