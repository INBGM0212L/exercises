# `P102113` - Prímteszt

Írjon programot, amely a standard bemenetről egy pozitív egész számot olvas be, majd eldönti, hogy az prím-e vagy sem!

## A bemenet specifikációja

A bemenet egy darab pozitív egész számot tartalmaz.

## A kimenet specifikációja

A programnak egy sort kell a standard kimenetre írnia, amely az `IGEN` vagy a `NEM` sztringet tartalmazza annak megfelelően, hogy a beolvasott szám prím-e vagy sem.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
2
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
IGEN
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
4
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
NEM
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
13
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
IGEN
```
