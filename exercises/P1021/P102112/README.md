# `P102112` - Relatív prímek

Írjon programot, amely a standard bemenetről két pozitív egész számot olvas be, majd eldönti, hogy relatív prímek-e vagy sem!

## A bemenet specifikációja

A bemenet két darab pozitív egész számot tartalmaz, melyek egy darab szóközzel vannak elválasztva.

## A kimenet specifikációja

A programnak egy sort kell a standard kimenetre írnia, amely az `IGEN` vagy a `NEM` sztringet tartalmazza annak megfelelően, hogy a két beolvasott szám relatív prím-e vagy sem.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
15 10
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
NEM
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
2 7
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
IGEN
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
124214 51255
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
IGEN
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
125 25
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
NEM
```
