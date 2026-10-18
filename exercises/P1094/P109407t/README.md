# `P109407t` - Kuponok #2 (végjelig olvasás)

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

## A(z) `coupon_to_line` függvény

Írj egy `coupon_to_line` nevű függvényt, mely megkap egy `Coupon` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `coupon` - a(z) `Coupon` típusú rekord

### Visszaadott érték

* az `coupon` paraméternek megfelelő sztring reprezentáció

### Példák

| `coupon` | Visszaadott érték |
| --- | --- |
| `Coupon(store='BiotechUSA', product='minden termek', discount=20)` | `"minden termek (BiotechUSA): 20%"`
| `Coupon(store='J.Press', product='teljes aru termekek', discount=20)` | `"teljes aru termekek (J.Press): 20%"`
| `Coupon(store='Media Markt', product='kavefozok', discount=20)` | `"kavefozok (Media Markt): 20%"`
| `Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)` | `"dekorkozmetikai termekek (Rossmann): 30%"`
| `Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)` | `"kiegeszitok (Samsung Experience Store): 20%"`

## A(z) `read_coupons_from_file` függvény

Írj egy `read_coupons_from_file` nevű függvényt, mely beolvassa egy szöveges fájlból, majd visszaadja a(z) `Coupon` típusú rekordok listáját!

### Paraméterlista

1. `file_name` - annak a fájlnak a neve (elérési útvonala), melyből a(z) `Coupon` típusú listát beolvassa a függvény (típusa: `<class 'str'>`)

### Visszaadott érték

* a beolvasott `Coupon` rekordok listája (típusa: `list[Coupon]`)


### Példa

* A(z) `file_name` paraméter értéke: `"bemenet.txt"`
* A(z) `"bemenet.txt"` szöveges fájl tartalma:
    ```
	Samsung Experience Store;kiegeszitok;20
	BiotechUSA;minden termek;20
	J.Press;teljes aru termekek;20
	Media Markt;kavefozok;20
	Rossmann;dekorkozmetikai termekek;30
    ```

* A függvény által visszaadott lista elemei:
    ```
	Coupon(store='Samsung Experience Store', product='kiegeszitok', discount=20)
	Coupon(store='BiotechUSA', product='minden termek', discount=20)
	Coupon(store='J.Press', product='teljes aru termekek', discount=20)
	Coupon(store='Media Markt', product='kavefozok', discount=20)
	Coupon(store='Rossmann', product='dekorkozmetikai termekek', discount=30)
    ```


## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A szöveges fájl sorai egy-egy `Coupon` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"END"`.
* A szöveges fájl beolvasása és feldolgozása a következő módon történik:
	* A főprogram a beolvasandó szöveges fájl nevét az első parancssori argumentumként kapja meg.
	1. A(z) főprogram meghívja a(z) `read_coupons_from_file()` függvényt, melynek átadja az első parancssori argumentumot.
	1. A(z) `read_coupons_from_file()` függvény megnyitja a paraméterként megkapott fájlt, majd a(z) `line_to_coupon` függvény felhasználásával beolvassa és visszaadja a(z) `Coupon` rekordok listáját.
	1. A(z) `Coupon` rekordok listája a(z) `sort_coupons()` függvénnyel rendezésre kerül.
	1. A(z) `Coupon` lista kiírása a(z) `coupon_to_line()` függvény felhasználásával.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |

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
minden termek (BiotechUSA): 20%
teljes aru termekek (J.Press): 20%
kavefozok (Media Markt): 20%
dekorkozmetikai termekek (Rossmann): 30%
kiegeszitok (Samsung Experience Store): 20%
```
