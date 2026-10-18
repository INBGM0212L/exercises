# `P102110` - Egészek maximuma #2

Írjon programot, amely a standard bemenetről egész számokat olvas, majd meghatározza azok maximumát!

## A bemenet specifikációja

A bemenet sorainak mindegyike egy-egy egész számot tartalmaz. A bemenet végét állományvégjel (`EOF`) jelzi.

## A kimenet specifikációja

A programnak egy sort kell a standard kimenetre írnia, amely a beolvasott egészek maximumát tartalmazza.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
1
2
5
-4
3
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
5
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
48
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
48
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
0
6
-11
8
0
6
-10
-12
-19
11
8
-8
-6
-15
-16
3
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
11
```
