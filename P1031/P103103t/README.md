# `P103103t` - Abszolút érték (végjelig olvasás)

## A függvény
Írj egy `absolute_value` nevű függvényt, mely visszaadja a paraméterként megkapott érték abszolőt értékét!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[-100,100]` intervallumból)

### Visszaadott érték
* az `n` abszolút értéke

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `-66` | `66` |
 | `11` | `11` |
 | `-91` | `91` |
 | `42` | `42` |
 | `20` | `20` |
 | `-42` | `42` |
 | `-77` | `77` |
 | `20` | `20` |
 | `-5` | `5` |


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
-66
11
-91
42
20
-42
-77
20
-5
999
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
66
11
91
42
20
42
77
20
5
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-65
84
-2
-68
-84
82
68
999
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
65
84
2
68
84
82
68
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-99
-81
-79
95
94
999
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
99
81
79
95
94
```
