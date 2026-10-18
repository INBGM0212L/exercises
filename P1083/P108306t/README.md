# `P108306t` - Kuponok #1 (végjelig olvasás)

## A feladat leírása
A kuponos akciók hatalmas tömegeket vonzanak a plázák üzleteibe, így történt ez a hétvégén is. Egy barátunk szeretne minél gyorsabban, minél nagyobb kedvezménnyel hozzájutni a szorgalmi időszak túléléséhez szükséges termékekhez. Sajnos azonban zárthelyi dolgozatra kell készülnie, így kevés időt tud a kuponok válogatására és beváltására fordítani. Egy olyan programra lenne szüksége, amely segít neki különböző szempontok szerint rendezni a magazinban található kuponokat.

Ebben a feladatban kuponok adatait kell beolvasnod a standard inputról, rendezni, majd kiírni a standard outputra.

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

| `entries` | Visszaadott érték |
| --- | --- |
| `"Samsung Experience Store;kiegeszitok;20"` | `Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)` |
| `"BiotechUSA;minden termek;20"` | `Coupon(store='BiotechUSA', product='minden termek', discount=20)` |
| `"J.Press;teljes aru termekek;20"` | `Coupon(store='J.Press', product='teljes aru termekek', discount=20)` |
| `"Media Markt;kavefozok;20"` | `Coupon(store='Media Markt', product='kavefozok', discount=20)` |
| `"Rossmann;dekorkozmetikai termekek;30"` | `Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)` |

## A(z) `coupon_to_line` függvény

Írj egy `coupon_to_line` nevű függvényt, mely megkap egy `Coupon` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `coupon` - a(z) `Coupon` típusú rekord

### Visszaadott érték

* az `coupon` paraméternek megfelelő sztring reprezentáció

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)` | `"dekorkozmetikai termekek (Rossmann): 30%"`
| `Coupon(store='BiotechUSA', product='minden termek', discount=20)` | `"minden termek (BiotechUSA): 20%"`
| `Coupon(store='J.Press', product='teljes aru termekek', discount=20)` | `"teljes aru termekek (J.Press): 20%"`
| `Coupon(store='Media Markt', product='kavefozok', discount=20)` | `"kavefozok (Media Markt): 20%"`
| `Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)` | `"kiegeszitok (Samsung Experience Store): 20%"`

## A(z) `sort_coupons` függvény

Írj egy `sort_coupons` nevű függvényt, mely megkap egy `Coupon` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `coupons` - a(z) `Coupon` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `coupons` lista a következő szempontok szerint rendezve:

	1. a kedvezmény mértéke szerint csökkenő sorrend
	1. az üzlet neve szerint növekvő sorrend
	1. termék neve szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20), Coupon(store='BiotechUSA', product='minden termek', discount=20), Coupon(store='J.Press', product='teljes aru termekek', discount=20), Coupon(store='Media Markt', product='kavefozok', discount=20), Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)]` | `[Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30), Coupon(store='BiotechUSA', product='minden termek', discount=20), Coupon(store='J.Press', product='teljes aru termekek', discount=20), Coupon(store='Media Markt', product='kavefozok', discount=20), Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)]` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Coupon` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"END"`.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. a(z) `Coupon` lista előállítása a(z) `line_to_coupon()` függvény felhasználásával
	1. a(z) `Coupon` lista rendezése a(z) `sort_coupons()` függvénnyel
	1. a(z) `Coupon` lista kiírása a(z) `coupon_to_line()` függvény felhasználásával

## Megjegyzés a *C* nyelvű megoldásokhoz

* A rendezéshez a `qsort()` függvényt használd.
* A(z) `coupon_to_line()` függvény a `qsort()` függvény negyedik paramétereként megadható, összehasonlító függvény.
* Minden dinamikusan foglalt területet fel kell szabadítani.
* A bemenet egyik sora sem hosszabb `1000` karakternél.
* A bemeneten legfeljebb `20` rekordot leíró sorra kell számítani.

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
dekorkozmetikai termekek (Rossmann): 30%
minden termek (BiotechUSA): 20%
teljes aru termekek (J.Press): 20%
kavefozok (Media Markt): 20%
kiegeszitok (Samsung Experience Store): 20%
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
I (K): 97%
L (G): 90%
H (L): 86%
W (I): 84%
I (C): 82%
H (O): 76%
U (A): 68%
K (J): 64%
R (N): 54%
V (M): 44%
Z (H): 42%
I (B): 39%
O (D): 33%
O (Q): 31%
O (F): 16%
F (P): 10%
D (E): 1%
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
D (D): 99%
X (E): 96%
Q (G): 90%
E (C): 84%
S (A): 50%
S (H): 36%
J (J): 32%
Z (K): 29%
K (F): 25%
W (B): 17%
A (I): 7%
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
J;E;55
A;W;90
C;W;16
H;V;9
G;H;77
F;U;5
K;Q;83
I;V;12
D;V;70
B;V;36
E;X;30
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
W (A): 90%
Q (K): 83%
H (G): 77%
V (D): 70%
E (J): 55%
V (B): 36%
X (E): 30%
W (C): 16%
V (I): 12%
V (H): 9%
U (F): 5%
```
