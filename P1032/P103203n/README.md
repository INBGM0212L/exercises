# `P103203n` - Relatív prímek (`n` teszteset)

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
* A tesztesetek száma az első sorban szereplő egész érték.
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
6
28 19
24 59
57 50
63 38
96 63
6 28
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
4
95 3
82 33
32 15
7 44
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
9
75 28
71 59
27 87
98 31
40 88
71 74
7 56
40 92
7 89
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
