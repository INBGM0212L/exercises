# `P102105` - Egészek átlaga #2

Írjon programot, amely a standard bemenetről egész számokat olvas, majd meghatározza azok átlagát!

## A bemenet specifikációja

A bemenet sorainak mindegyike egy-egy egész számot tartalmaz. A bemenet végét állományvégjel (`EOF`) jelzi.

## A kimenet specifikációja

A programnak egy sort kell a standard kimenetre írnia, amely az `n` szám átlagát tartalmazza két tizedesjegy pontossággal.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
-2
-1
0
1
2
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
0.00
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
251
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
251.00
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
-3.44
```
