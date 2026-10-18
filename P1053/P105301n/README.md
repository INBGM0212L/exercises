# `P105301n` - Kisbetűk inkrementálása (`n` teszteset)

## A függvény
Írj egy `increment_lowers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring kisbetűinek inkrementálásával kapunk!

### Magyarázat
Egy kisbetű inkrementálása alatt azt a műveletet értjük, mely során a betűt az ábécében őt követő kisbetűvel helyettesítjük. Például az `a` karaktert a `b` karakterre, míg a `b` karaktert a `c` karakterre cseréljük. A `z` karaktert az `a` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"bcdefghijklmnopqrstuvwxyza"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"b·c·d·e·f·g·h·i"` |
 | `"aA······bB"` | `"bA······cB"` |
 | `"A··a·····b···B"` | `"A··b·····c···B"` |
 | `"aB1cD2eF3gH4"` | `"bB1dD2fF3hH4"` |

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
bcdefghijklmnopqrstuvwxyza
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
b c d e f g h i
bA      cB
A  b     c   B
bB1dD2fF3hH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
3
qy4pA
ZscykaMornmWka
l1NWxazG3vZcdzOowJ4up
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
rz4qA
ZtdzlbMpsonWlb
m1NWybaG3wZdeaOpxJ4vq
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
9
rJcYUjkjwq B
wB
CAxnRpeojygajscnYZ5hQysW4RyU
vkfjxeqI4rKov
x
rcBsnVElpz3lm2vhcrCwajW9jE
hf2pZyz1dN
Pkmrkq6C pV33lmswo5mRbaud t5v
iGb
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
sJdYUklkxr B
xB
CAyoRqfpkzhbktdoYZ5iQztW4RzU
wlgkyfrI4sKpw
y
sdBtoVEmqa3mn2widsCxbkW9kE
ig2qZza1eN
Plnslr6C qV33mntxp5nRcbve u5w
jGc
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
7
dmgghrqdPwPv1rym9tkpcD
hqFbzgcHx5
otvJwihTVb8pKWlzqGYyAmrvv
cuR3
ivfysZbNXe
tQdtl
etRkfcltyu
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
enhhisrePxPw1szn9ulqdD
irFcahdHy5
puwJxjiTVc8qKWmarGYzAnsww
dvR3
jwgztZcNXf
uQeum
fuRlgdmuzv
```
