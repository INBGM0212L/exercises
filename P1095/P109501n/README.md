# `P109501n` - Minyonok (`n` teszteset)

## A feladat leírása
A minyonok története az idők kezdetétől ered. A minyonok sárga egysejtű organizmusként kezdték, és fejlődtek a korokon át, és mindig a leggrúsabb gazdákat szolgálták. Mivel ezeket a gazdákat – a T-Rextől Napóleonig – folytonosan elveszítették, a minyonoknak most nincs kit szolgálniuk, és mély depresszióba zuhantak.

Ebben a feladatban minyonok adatai kell beolvasnod a standard inputról, majd feldolgozni a beolvasott listát.

## Formátumok

* A standard bemeneten egy minyon a következő formátumban szerepel:

    ```
    minyon_neve;éhség;lelkesedés;nadrág_mérete
    ```

* A standard kimeneten egy minyon a következő formátumban szerepel:

    ```
    minyon_neve éhség (nadrág_mérete)
    ```

* A jelölések:

  * A `minyon_neve` egy legfeljebb `30` karakter hosszú, csak angol betűket tartalmazó egyedi sztring.
  * Az `éhség` és a `lelkesedés` egyaránt `0` és `100` közötti egész szám.
  * A `nadrág_mérete` az `"S"`, `"L"`, `"XL"` és "`XXL`" sztringek egyike.

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `Minion` típus
Definiáld a `Minion` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `name`: a minyon neve (típus: `<class 'str'>`)
* `hunger`: a minyon éhsége (típus: `<class 'int'>`)
* `motivation`: a minyon motiváltsága (típus: `<class 'int'>`)
* `size`: a minyon mérete (típus: `<class 'str'>`)

## A(z) `line_to_minion` függvény
Írj egy `line_to_minion` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `Minion` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `Minion` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `Minion` rekord

### Példák

| `line` | Visszaadott érték |
| --- | --- |
| `"Bob;87;100;S"` | `Minion(name='Bob', hunger=87, motivation=100, size='S')` |
| `"Dave;43;10;L"` | `Minion(name='Dave', hunger=43, motivation=10, size='L')` |
| `"Stuart;50;30;L"` | `Minion(name='Stuart', hunger=50, motivation=30, size='L')` |
| `"Jerry;40;20;XL"` | `Minion(name='Jerry', hunger=40, motivation=20, size='XL')` |

## A(z) `minion_to_line` függvény

Írj egy `minion_to_line` nevű függvényt, mely megkap egy `Minion` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `minion` - a(z) `Minion` típusú rekord

### Visszaadott érték

* az `minion` paraméternek megfelelő sztring reprezentáció

### Példák

| `minion` | Visszaadott érték |
| --- | --- |
| `Minion(name='Bob', hunger=87, motivation=100, size='S')` | `"Bob 87 (S)"`
| `Minion(name='Dave', hunger=43, motivation=10, size='L')` | `"Dave 43 (L)"`
| `Minion(name='Stuart', hunger=50, motivation=30, size='L')` | `"Stuart 50 (L)"`
| `Minion(name='Jerry', hunger=40, motivation=20, size='XL')` | `"Jerry 40 (XL)"`

## A(z) `distinct_motivations` függvény

Írj egy `distinct_motivations` nevű függvényt, mely visszaadja azokat az értékeket, melyek előfordulnak a minyonok motiváltságaként!

### Paraméterlista

1. `minions` - a(z) `Minion` elemeket tartalmazó lista (típusa: `list[Minion]`)

### Visszaadott érték

* egy halmaz, mely a `minions` paraméterben előforduló motiváltsági értékeket tartalmazza (típusa: `set[int]`)


### Példák

| `minions` | Visszaadott érték |
| --- | --- |
| `[Minion(name='Bob', hunger=87, motivation=100, size='S'), Minion(name='Dave', hunger=43, motivation=10, size='L'), Minion(name='Stuart', hunger=50, motivation=30, size='L'), Minion(name='Jerry', hunger=40, motivation=20, size='XL')]` | `[10, 100, 20, 30]` |

## A(z) `read_minions_from_file` függvény

Írj egy `read_minions_from_file` nevű függvényt, mely beolvassa egy szöveges fájlból, majd visszaadja a(z) `Minion` típusú rekordok listáját!

### Paraméterlista

1. `file_name` - annak a fájlnak a neve (elérési útvonala), melyből a(z) `Minion` típusú listát beolvassa a függvény (típusa: `<class 'str'>`)

### Visszaadott érték

* a beolvasott `Minion` rekordok listája (típusa: `list[Minion]`)


### Példa

* A(z) `file_name` paraméter értéke: `"bemenet.txt"`
* A(z) `"bemenet.txt"` szöveges fájl tartalma:
    ```
	Bob;87;100;S
	Dave;43;10;L
	Stuart;50;30;L
	Jerry;40;20;XL
    ```

* A függvény által visszaadott lista elemei:
    ```
	Minion(name='Bob', hunger=87, motivation=100, size='S')
	Minion(name='Dave', hunger=43, motivation=10, size='L')
	Minion(name='Stuart', hunger=50, motivation=30, size='L')
	Minion(name='Jerry', hunger=40, motivation=20, size='XL')
    ```


## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A szöveges fájl sorai egy-egy `Minion` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A szöveges fájl első sora tartalmazza a feldolgozandó sorok számát (`n`).
* Az első sort pontosan `n` darab, a feladat szövegének megfelelő sor követi.
* A szöveges fájl beolvasása és feldolgozása a következő módon történik:
	* A főprogram a beolvasandó szöveges fájl nevét az első parancssori argumentumként kapja meg.
	1. A(z) főprogram meghívja a(z) `read_minions_from_file()` függvényt, melynek átadja az első parancssori argumentumot.
	1. A(z) `read_minions_from_file()` függvény megnyitja a paraméterként megkapott fájlt, majd a(z) `line_to_minion` függvény felhasználásával beolvassa és visszaadja a(z) `Minion` rekordok listáját.
	1. A(z) `distinct_motivations()` függvény meghívása.
	2. A visszakapott halmaz elemeinek kiírása. Minden érték a kimenet egy külön sorába kerül.

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
4
Bob;87;100;S
Dave;43;10;L
Stuart;50;30;L
Jerry;40;20;XL
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
10
100
20
30
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
11
I;1;27;M
C;26;2;L
G;35;79;XXL
D;80;34;XXL
F;12;32;XL
E;54;95;XL
B;45;27;S
H;21;29;XXL
K;10;55;L
J;37;99;L
A;1;83;S
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
32
2
34
99
79
83
55
27
29
95
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
11
F;30;46;XL
I;53;31;XXL
G;54;21;L
H;21;71;XL
A;97;73;XXL
J;62;18;M
B;51;60;L
C;100;59;L
K;61;67;XXL
E;50;67;S
D;75;34;S
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
34
67
71
73
46
18
21
59
60
31
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
10
E;8;12;XL
J;5;77;XL
G;26;66;S
D;54;98;S
F;37;16;XL
I;37;22;M
A;97;24;M
B;79;57;M
H;76;13;M
C;48;69;L
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
66
98
69
12
77
13
16
22
24
57
```
