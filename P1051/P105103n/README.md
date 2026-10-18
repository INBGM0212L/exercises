# `P105103n` - Nagybetűk eltávolítása (`n` teszteset)

## A függvény
Írj egy `delete_uppers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring nagybetűinek törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `""` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"a······b"` |
 | `"A··a·····b···B"` | `"··a·····b···"` |
 | `"aB1cD2eF3gH4"` | `"a1c2e3g4"` |

A paraméterekhez tartozó literálokban minden `' '` (szóköz) karakter a `'·'` (pont) karakterrel kerül helyettesítésre.


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`original`) szerepel.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.

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
7
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
a b c d e f g h
aA      bB
A  a     b   B
aB1cD2eF3gH4
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
abcdefghijklmnopqrstuvwxyz

0123456789
a b c d e f g h
a      b
  a     b   
a1c2e3g4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
8
ETrFa9CZR7QYfSZQFFmU
G
JHXTVak2LXVUErSNrO
MvzJUYLqWSViBV
xPJ2T2MfYXKSHk7ZgPzlBNySFQPJ
Y7D qZrP6FtgM
ZTtsOXGKmHtbHg2QCUIRAl9pVwhsT
XPEOhL0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
ra97fm

ak2rr
vzqi
x22fk7gzly
7 qr6tg
tsmtbg2l9pwhs
h0
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
10
T1 KFAqEgltjZVsZJ
AjOGRXnGgUVi
nWKsNBxbImWFClMlgMcE7BUQTZGAA
XAVpvVGgGUQVLLDm3BIUQ
GNJM
KgmqZ6CH VV45DFNDLFOYXI
T
6UKDOK6YeHL GP
vJeMlERGBC4N
LuYQjCGdWuanZ4mkRT
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
1 qgltjs
jngi
nsxbmllgc7
pvgm3

gmq6 45

66e 
vel4
ujduan4mk
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
10
LbNAIbnG5BNyQqfxWGV4oWYT ZM4
KSMiR
HOctBzNyM2nMDTC4XYtpTvU4NMOL
AxOCuwQALUeXOLdXUPZH
cXWOIFJSogFD1uwYQDvCOYksMc7GT
RPJT5ZbS
vTC
VMZGOX0PYX
X8XM XI2YUg
KGDrxD 1
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
bbn5yqfx4o 4
i
ctzy2n4tpv4
xuwed
cog1uwvksc7
5b
v
0
8 2g
rx 1
```
