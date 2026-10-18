# `P108307n` - Kuponok #2 (`n` teszteset)

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
| `Coupon(store='BiotechUSA', product='minden termek', discount=20)` | `"minden termek (BiotechUSA): 20%"`
| `Coupon(store='J.Press', product='teljes aru termekek', discount=20)` | `"teljes aru termekek (J.Press): 20%"`
| `Coupon(store='Media Markt', product='kavefozok', discount=20)` | `"kavefozok (Media Markt): 20%"`
| `Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)` | `"dekorkozmetikai termekek (Rossmann): 30%"`
| `Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)` | `"kiegeszitok (Samsung Experience Store): 20%"`

## A(z) `sort_coupons` függvény

Írj egy `sort_coupons` nevű függvényt, mely megkap egy `Coupon` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `coupons` - a(z) `Coupon` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `coupons` lista a következő szempontok szerint rendezve:

	1. az üzlet neve szerint növekvő sorrend
	1. a kedvezmény mértéke szerint csökkenő sorrend
	1. termék neve szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20), Coupon(store='BiotechUSA', product='minden termek', discount=20), Coupon(store='J.Press', product='teljes aru termekek', discount=20), Coupon(store='Media Markt', product='kavefozok', discount=20), Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)]` | `[Coupon(store='BiotechUSA', product='minden termek', discount=20), Coupon(store='J.Press', product='teljes aru termekek', discount=20), Coupon(store='Media Markt', product='kavefozok', discount=20), Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30), Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)]` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Coupon` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A standard bemenet első sora tartalmazza a feldolgozandó sorok számát (`n`).
* Az első sort pontosan `n` darab, a feladat szövegének megfelelő sor követi.
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
5
Samsung Experience Store;kiegeszitok;20
BiotechUSA;minden termek;20
J.Press;teljes aru termekek;20
Media Markt;kavefozok;20
Rossmann;dekorkozmetikai termekek;30
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
minden termek (BiotechUSA): 20%
teljes aru termekek (J.Press): 20%
kavefozok (Media Markt): 20%
dekorkozmetikai termekek (Rossmann): 30%
kiegeszitok (Samsung Experience Store): 20%
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
16
J;G;47
B;C;11
E;C;11
G;A;89
A;M;64
I;M;47
L;T;24
C;Y;23
H;H;50
N;O;59
D;N;16
M;V;76
F;U;73
P;F;91
O;P;92
K;D;3
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
M (A): 64%
C (B): 11%
Y (C): 23%
N (D): 16%
C (E): 11%
U (F): 73%
A (G): 89%
H (H): 50%
M (I): 47%
G (J): 47%
D (K): 3%
T (L): 24%
V (M): 76%
O (N): 59%
P (O): 92%
F (P): 91%
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
16
H;S;64
O;A;15
P;R;56
K;M;67
M;E;12
F;I;52
E;M;63
G;U;37
B;C;85
N;T;36
A;P;100
C;B;73
L;P;73
I;P;61
D;W;39
J;C;63
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
P (A): 100%
C (B): 85%
B (C): 73%
W (D): 39%
M (E): 63%
I (F): 52%
U (G): 37%
S (H): 64%
P (I): 61%
C (J): 63%
M (K): 67%
P (L): 73%
E (M): 12%
T (N): 36%
A (O): 15%
R (P): 56%
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
19
J;U;92
D;V;59
G;Q;78
Q;Q;78
L;G;85
F;N;66
P;F;48
I;T;34
S;Y;79
N;A;42
K;X;5
A;O;24
O;I;94
C;A;63
M;J;92
R;W;17
E;D;59
H;K;73
B;I;88
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
O (A): 24%
I (B): 88%
A (C): 63%
V (D): 59%
D (E): 59%
N (F): 66%
Q (G): 78%
K (H): 73%
T (I): 34%
U (J): 92%
X (K): 5%
G (L): 85%
J (M): 92%
A (N): 42%
I (O): 94%
F (P): 48%
Q (Q): 78%
W (R): 17%
Y (S): 79%
```
