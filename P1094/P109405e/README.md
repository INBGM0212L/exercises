# `P109405e` - LEGO készletek #2 (állományvégjelig olvasás)

## A feladat leírása
Egy játékbolt polcain több különböző témájú és méretű Lego készlet közül válogathatunk. Ezek lehetnek kicsi zacskósak, de akár hatalmas dobozosok is. A megvásárolandó készlet kiválasztása éppen ezért sokszor hatalmas fejtörést okoz.

Ebben a feladatban LEGO készletek adatait kell beolvasnod a standard inputról, majd feldolgozni a beolvasott listát.

## Formátumok

* A standard bemeneten egy LEGO készlet a következő formátumban szerepel:
    ```
    <termékkód>;<szett_neve>;<téma_neve>;<elemek_száma>
    ```

* A standard kimeneten egy LEGO készlet a következő formátumban szerepel:
    ```
    <szett_neve> (<termékkód>): <elemek_száma> - <téma_neve>
    ```

* A jelölések:
  * `termékkód`: egy negmnegatív egész érték
  * `szett_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `téma_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `elemek_száma`: egy nemnegatív egész érték

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `LegoSet` típus
Definiáld a `LegoSet` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `number`: a készlet kódja (típus: `<class 'int'>`)
* `name`: a készlet neve (típus: `<class 'str'>`)
* `theme`: a téma neve (típus: `<class 'str'>`)
* `pieces`: az elemek száma (típus: `<class 'int'>`)

## A(z) `line_to_lego_set` függvény
Írj egy `line_to_lego_set` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `LegoSet` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `LegoSet` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `LegoSet` rekord

### Példák

| `line` | Visszaadott érték |
| --- | --- |
| `"30356;Hot dog arus;Lego City;43"` | `LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43)` |
| `"30360;Sarkvideki jegfuresz;Lego City;43"` | `LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43)` |
| `"30381;Birodalmi TIE Fighter;Lego Star Wars;42"` | `LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)` |
| `"10258;London Bus;Lego Creator Expert;1686"` | `LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686)` |
| `"10253;Big Ben;Lego Creator Expert;4163"` | `LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)` |

## A(z) `lego_set_to_line` függvény

Írj egy `lego_set_to_line` nevű függvényt, mely megkap egy `LegoSet` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `lego_set` - a(z) `LegoSet` típusú rekord

### Visszaadott érték

* az `lego_set` paraméternek megfelelő sztring reprezentáció

### Példák

| `lego_set` | Visszaadott érték |
| --- | --- |
| `LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43)` | `"Hot dog arus (30356): 43 - Lego City"`
| `LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43)` | `"Sarkvideki jegfuresz (30360): 43 - Lego City"`
| `LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)` | `"Big Ben (10253): 4163 - Lego Creator Expert"`
| `LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686)` | `"London Bus (10258): 1686 - Lego Creator Expert"`
| `LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)` | `"Birodalmi TIE Fighter (30381): 42 - Lego Star Wars"`

## A(z) `read_lego_sets_from_file` függvény

Írj egy `read_lego_sets_from_file` nevű függvényt, mely beolvassa egy szöveges fájlból, majd visszaadja a(z) `LegoSet` típusú rekordok listáját!

### Paraméterlista

1. `file_name` - annak a fájlnak a neve (elérési útvonala), melyből a(z) `LegoSet` típusú listát beolvassa a függvény (típusa: `<class 'str'>`)

### Visszaadott érték

* a beolvasott `LegoSet` rekordok listája (típusa: `list[LegoSet]`)


### Példa

* A(z) `file_name` paraméter értéke: `"bemenet.txt"`
* A(z) `"bemenet.txt"` szöveges fájl tartalma:
    ```
	30356;Hot dog arus;Lego City;43
	30360;Sarkvideki jegfuresz;Lego City;43
	30381;Birodalmi TIE Fighter;Lego Star Wars;42
	10258;London Bus;Lego Creator Expert;1686
	10253;Big Ben;Lego Creator Expert;4163
    ```

* A függvény által visszaadott lista elemei:
    ```
	LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43)
	LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43)
	LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)
	LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686)
	LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)
    ```


## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A szöveges fájl sorai egy-egy `LegoSet` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* A szöveges fájl beolvasása és feldolgozása a következő módon történik:
	* A főprogram a beolvasandó szöveges fájl nevét az első parancssori argumentumként kapja meg.
	1. A(z) főprogram meghívja a(z) `read_lego_sets_from_file()` függvényt, melynek átadja az első parancssori argumentumot.
	1. A(z) `read_lego_sets_from_file()` függvény megnyitja a paraméterként megkapott fájlt, majd a(z) `line_to_lego_set` függvény felhasználásával beolvassa és visszaadja a(z) `LegoSet` rekordok listáját.
	1. A(z) `LegoSet` rekordok listája a(z) `sort_lego_sets()` függvénnyel rendezésre kerül.
	1. A(z) `LegoSet` lista kiírása a(z) `lego_set_to_line()` függvény felhasználásával.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
30356;Hot dog arus;Lego City;43
30360;Sarkvideki jegfuresz;Lego City;43
30381;Birodalmi TIE Fighter;Lego Star Wars;42
10258;London Bus;Lego Creator Expert;1686
10253;Big Ben;Lego Creator Expert;4163
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
Hot dog arus (30356): 43 - Lego City
Sarkvideki jegfuresz (30360): 43 - Lego City
Big Ben (10253): 4163 - Lego Creator Expert
London Bus (10258): 1686 - Lego Creator Expert
Birodalmi TIE Fighter (30381): 42 - Lego Star Wars
```
