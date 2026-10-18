# `P109206t` - Kuponok #1 (végjelig olvasás)

## A feladat leírása
A kuponos akciók hatalmas tömegeket vonzanak a plázák üzleteibe, így történt ez a hétvégén is. Egy barátunk szeretne minél gyorsabban, minél nagyobb kedvezménnyel hozzájutni a szorgalmi időszak túléléséhez szükséges termékekhez. Sajnos azonban zárthelyi dolgozatra kell készülnie, így kevés időt tud a kuponok válogatására és beváltására fordítani. Egy olyan programra lenne szüksége, amely segít neki különböző szempontok szerint rendezni a magazinban található kuponokat.

Ebben a feladatban kuponok adatait kell beolvasnod a standard inputról, majd feldolgozni a beolvasott listát.

## Formátumok

* A standard bemeneten egy kupono a következő formátumban szerepel:
    ```
    <üzlet_neve>;<termék_neve>;<kedvezmény_mértéke>
    ```

* A standard kimeneten egy kupon a következő formátumban szerepel:
    ```
    <termék_neve> (<üzlet_neve>): <kedvezmény_mértéke>%
    ```

* A jelölések:
  * `üzlet_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `termék_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `kedvezmény_mértéke`: egy nemnegatív egész érték

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `Coupon` típus
Definiáld a `Coupon` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `store`: az üzlet neve (típus: `<class 'str'>`)
* `product`: a termék neve (típus: `<class 'str'>`)
* `discount`: a kedvezmény mértéke (típus: `<class 'int'>`)

## A(z) `line_to_coupon` függvény
Írj egy `line_to_coupon` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `Coupon` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `Coupon` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `Coupon` rekord

### Példák

| `line` | Visszaadott érték |
| --- | --- |
| `"Samsung Experience Store;kiegeszitok;20"` | `Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)` |
| `"BiotechUSA;minden termek;20"` | `Coupon(store='BiotechUSA', product='minden termek', discount=20)` |
| `"J.Press;teljes aru termekek;20"` | `Coupon(store='J.Press', product='teljes aru termekek', discount=20)` |
| `"Media Markt;kavefozok;20"` | `Coupon(store='Media Markt', product='kavefozok', discount=20)` |
| `"Rossmann;dekorkozmetikai termekek;30"` | `Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)` |

## A(z) `count_by_discounts` függvény

Írj egy `count_by_discounts` nevű függvényt, mely visszaadja azt, hogy a `coupons` paraméterként megkapott listában hány kupon tartozik az egyes kedvezményekhez!

### Paraméterlista

1. `coupons` - a(z) `Coupon` elemeket tartalmazó lista (típusa: `list[Coupon]`)

### Visszaadott érték

* egy szótár, melynek a kulcsai a kedvezmények, egy-egy értéke pedig az adott kedvezményhez tartozó kuponok száma (típusa: `dict[int, int]`)


### Példák

| `coupons` | Visszaadott érték |
| --- | --- |
| `[Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20), Coupon(store='BiotechUSA', product='minden termek', discount=20), Coupon(store='J.Press', product='teljes aru termekek', discount=20), Coupon(store='Media Markt', product='kavefozok', discount=20), Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)]` | `{'20': 4, '30': 1}` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Coupon` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"END"`.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. A(z) `Coupon` lista előállítása a(z) `line_to_coupon()` függvény felhasználásával.
	1. A(z) `count_by_discounts()` függvény meghívása.
	1. A visszakapott szótár bejegyzéseinek kiírása. Minden bejegyzés egy külön, `<kulcs>: <érték>` formátumú sorba kerüljön, ahol a `kulcs` a szótár egy kulcsa, az `érték` pedig a kulcshoz tartozó érték.

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
Samsung Experience Store;kiegeszitok;20
BiotechUSA;minden termek;20
J.Press;teljes aru termekek;20
Media Markt;kavefozok;20
Rossmann;dekorkozmetikai termekek;30
END
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
20: 4
30: 1
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
B;I;39
N;R;54
Q;O;31
C;I;82
D;O;33
H;Z;42
P;F;10
J;K;64
F;O;16
O;H;76
L;H;86
G;L;90
M;V;44
E;D;1
I;W;84
K;I;97
A;U;68
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
39: 1
54: 1
31: 1
82: 1
33: 1
42: 1
10: 1
64: 1
16: 1
76: 1
86: 1
90: 1
44: 1
1: 1
84: 1
97: 1
68: 1
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
I;A;7
H;S;36
C;E;84
D;D;99
E;X;96
B;W;17
K;Z;29
A;S;50
G;Q;90
J;J;32
F;K;25
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
7: 1
36: 1
84: 1
99: 1
96: 1
17: 1
29: 1
50: 1
90: 1
32: 1
25: 1
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
J;E;55
A;W;90
C;W;5
H;V;9
G;H;77
F;U;5
K;Q;12
I;V;12
D;V;70
B;V;30
E;X;30
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
55: 1
90: 1
5: 2
9: 1
77: 1
12: 2
70: 1
30: 2
```
