# `P105106n` - Mássalhangzók eltávolítása (`n` teszteset)

## A függvény
Írj egy `delete_consonants` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring mássalhangzóinak törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"aeiou"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"AEIOU"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a····e···"` |
 | `"aA······bB"` | `"aA······"` |
 | `"A··a·····b···B"` | `"A··a········"` |
 | `"aB1cD2eF3gH4"` | `"a12e34"` |

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
aeiou
AEIOU
0123456789
a    e   
aA      
A  a        
a12e34
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
10
zrcJ
mjgHtMd8xBw
hoHvqiph3A
jcQdvywDns
w0jltxk
4FqplgShsmdxizvlApdckzdbvn
18GxzCd9pFVRwfqy
lpny6x2ghwErFwpc048rv1Qx0g ly
rv5rvOggMdQlcjxg
lfA5ADs8vkSpsyqsdrn
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```

8
oi3A

0
4iA
189
62E04810 
5O
A5A8
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
6
dxJlrN5JC
ZcwY0ftMkmAlljCbqwo
FvdinOthCvUzmakmWvr3qsgghwz
xziwywhm6IgkdrysbkbfSt3uflmpX
wdmbnertKfvmLRllmdzhmvftTsdx
n
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
5
0Ao
iOUa3
i6I3u
e
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
9
bclgQ2nGOcxm6akEm6AbrVl5
hIlppqkvSYwWd7wSahntKndtsrneX
lshphbppL
Rkykh tsmzqqztxhrA
bxfzQfdfupfRclbEzdtxFk
cxzatgtdCjmtybzK4jbWGrix
djKhmdlZ0bocyVvVy6I4 jlTyv
jbhxYhp7UqkZvgisjh5roH88
0vwjb
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
2O6aE6A5
I7ae

 A
uE
a4i
0o6I4 
7Ui5o88
0
```
