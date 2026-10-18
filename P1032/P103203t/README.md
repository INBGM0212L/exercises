# `P103203t` - Relatív prímek (végjelig olvasás)

## A függvény
Írj egy `are_relative_primes` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott két szám (`a` és `b`) relatív prímek-e vagy sem!


### Paraméterlista
1. `a` - az `a` értéke (egész érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` értéke (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* `True`, ha `a` és `b` relatív prímek, egyébként `False`

### Példák
 | `a` | `b` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `28` | `19` | `True` |
 | `24` | `59` | `True` |
 | `57` | `50` | `True` |
 | `63` | `38` | `True` |
 | `96` | `63` | `False` |
 | `6` | `28` | `False` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`
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
28 19
24 59
57 50
63 38
96 63
6 28
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
True
True
True
True
False
False
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
95 3
82 33
32 15
7 44
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
True
True
True
True
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
75 28
71 59
27 87
98 31
40 88
71 74
7 56
40 92
7 89
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
True
True
False
True
False
True
False
False
True
```
