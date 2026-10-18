# `P102106` - Egészek átlaga #3

Írjon programot, amely a standard bemenetről egész számokat olvas, majd meghatározza azok átlagát!

## A bemenet specifikációja

A bemenet sorainak mindegyike egy-egy egész számot tartalmaz. A beolvasás mindaddig folytatódjon, míg a beolvasott érték nem 0! A bemenet végét jelző `0` értéket ne vegye figyelembe az átlag kiszámításánál!

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
1
2
0
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
0.00
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
-192
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
-192.00
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
16
2
6
-11
8
1
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
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
-2.12
```
