# `P103205n` - `n` összeg (`n` teszteset)

## A függvény
Írj egy `n_sum` nevű függvényt, mely visszaadja az első `n` pozitív egész összegét!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[0,1000]` intervallumból)

### Visszaadott érték
* az első `n` pozitív egész szám összege

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `53` | `1431` |
 | `373` | `69751` |
 | `10` | `55` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`n`) szerepel.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
3
53
373
10
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1431
69751
55
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
7
82
121
461
766
912
808
981
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
3403
7381
106491
293761
416328
326836
481671
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
5
46
853
263
798
669
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
1081
364231
34716
318801
224115
```
