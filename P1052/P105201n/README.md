# `P105201n` - Szóközök duplikálása (`n` teszteset)

## A függvény
Írj egy `double_spaces` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring szóközeinek megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a··b··c··d··e··f··g··h"` |
 | `"aA······bB"` | `"aA············bB"` |
 | `"A··a·····b···B"` | `"A····a··········b······B"` |
 | `"aB1cD2eF3gH4"` | `"aB1cD2eF3gH4"` |

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
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
a  b  c  d  e  f  g  h
aA            bB
A    a          b      B
aB1cD2eF3gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
9
EbR zJZgRpRS 
usFvz8PyF D Ol qR 
5gGrjXu   gSO ubSy 
9f im5Et9j 
L SebSkykd0Ar8 w1GEh fzUprAN
W7ZG YfsI  KPE6  ZH
n b  
9Xs
V0T4k5RKD5 dZOUWr7 UbmSR5C
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
EbR  zJZgRpRS  
usFvz8PyF  D  Ol  qR  
5gGrjXu      gSO  ubSy  
9f  im5Et9j  
L  SebSkykd0Ar8  w1GEh  fzUprAN
W7ZG  YfsI    KPE6    ZH
n  b    
9Xs
V0T4k5RKD5  dZOUWr7  UbmSR5C
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5
H  hbQ6f   9 HEvEJoWfGv
bUd  e Vjl5 eqYt7 d
wQ 9uDuw5 lP Dox  4
w H NWwrxgj dfiWUzVkj9A
 voq
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
H    hbQ6f      9  HEvEJoWfGv
bUd    e  Vjl5  eqYt7  d
wQ  9uDuw5  lP  Dox    4
w  H  NWwrxgj  dfiWUzVkj9A
  voq
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8
Etjt KxI
y  BAi56 eXUj 5mQaU0YMWWg 
GkhB53JTo9HbK29My  k
X 4dj9H tDoH Wa
3AH5k6 Be5TF9 C3Z7Bkvz 7B 5N
j6kSQKdO0Yd5 V8f 4wERPZl
s  pr
2k Zs0xq 
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
Etjt  KxI
y    BAi56  eXUj  5mQaU0YMWWg  
GkhB53JTo9HbK29My    k
X  4dj9H  tDoH  Wa
3AH5k6  Be5TF9  C3Z7Bkvz  7B  5N
j6kSQKdO0Yd5  V8f  4wERPZl
s    pr
2k  Zs0xq  
```
