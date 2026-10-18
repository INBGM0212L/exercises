# `P103215t` - Mértani sorozat `n`. eleme (végjelig olvasás)

## A függvény
Írj egy `geometric_sequence_element` nevű függvényt, mely visszaadja az (`a`, `q`) paraméterű mértani sorozat `n`. elemét!


### Paraméterlista
1. `a` - a sorozat első eleme (egész érték a(z) `[1,100]` intervallumból)
2. `n` - az `n` értéke (egész érték a(z) `[1,50]` intervallumból)
3. `q` - a sorozat kvóciense (egész érték a(z) `[1,10]` intervallumból)

### Visszaadott érték
* a sorozat `n`. eleme

### Példák
 | `a` | `n` | `q` | Visszaadott érték |
 | :--- | :--- | :--- | :-- |
 | `97` | `28` | `1` | `97` |
 | `9` | `30` | `5` | `1676380634307861328125` |
 | `96` | `33` | `3` | `177889938129776736` |
 | `37` | `14` | `7` | `3584893385059` |
 | `52` | `9` | `7` | `299769652` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`a`, `n` és `q`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
97 28 1
9 30 5
96 33 3
37 14 7
52 9 7
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
97
1676380634307861328125
177889938129776736
3584893385059
299769652
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
16 5 1
61 4 10
13 5 10
29 38 3
2 34 9
21 6 2
17 43 9
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
16
61000
130000
13058233270838923527
61806308765265224723841283607058
672
203532758103554336406246580454189800796577
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
62 46 3
84 7 6
63 20 2
60 1 7
97 25 9
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
183167387806151689315866
3919104
33030144
60
7737344978456633456746017
```
