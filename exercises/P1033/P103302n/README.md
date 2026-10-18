# `P103302n` - Rekurzív `n` összeg (`n` teszteset)

## A függvény
Írj egy `n_sum` nevű függvényt, mely visszaadja az első `n` pozitív egész összegét! A függvény rekurzív módon határozza meg az eredményt!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[0,1000]` intervallumból)

### Visszaadott érték
* az első `n` pozitív egész szám összege

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `21` | `232` |
 | `279` | `39061` |
 | `205` | `21116` |
 | `328` | `53957` |
 | `641` | `205762` |
 | `775` | `300701` |
 | `99` | `4951` |
 | `380` | `72391` |


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
8
21
279
205
328
641
775
99
380
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
232
39061
21116
53957
205762
300701
4951
72391
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5
341
3
963
316
22
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
58312
7
464167
50087
254
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
5
14
91
616
479
676
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
106
4187
190037
114961
228827
```
