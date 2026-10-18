# `P102109` - Egészek maximuma #1

Írjon programot, amely a standard bemenetről egész számokat olvas, majd meghatározza azok maximumát!

## A bemenet specifikációja

A bemenet első sora egy `n` pozitív egészet tartalmaz, melyet `n` darab egész szám követ (soronként egy).

## A kimenet specifikációja

A programnak egy sort kell a standard kimenetre írnia, amely az `n` szám maximumát tartalmazza.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
5
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
1
48
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
48
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
16
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
