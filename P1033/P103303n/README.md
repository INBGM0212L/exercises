# `P103303n` - Rekurzív Fibonacci (`n` teszteset)

## A függvény
Írj egy `n_fibonacci` nevű függvényt, mely visszaadja a Fibonacci-sorozat `n`. elemét! A függvény rekurzív módon határozza meg az eredményt!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[0,30]` intervallumból)

### Visszaadott érték
* az `n`. Fibonacci szám

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `9` | `55` |
 | `14` | `610` |
 | `29` | `832040` |
 | `23` | `46368` |
 | `26` | `196418` |
 | `16` | `1597` |
 | `9` | `55` |
 | `26` | `196418` |
 | `27` | `317811` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`n`) szerepel.

## Megjegyzés a *C* nyelvű megoldásokhoz
A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. A *C* nyelv típusaival nem ábrázolható az összes példákban szereplő érték.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
9
9
14
29
23
26
16
9
26
27
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
55
610
832040
46368
196418
1597
55
196418
317811
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
10
22
13
15
26
21
24
4
10
26
22
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
28657
377
987
196418
17711
75025
5
89
196418
28657
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
4
29
2
15
15
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
832040
2
987
987
```
