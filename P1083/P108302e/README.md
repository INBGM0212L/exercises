# `P108302e` - Hullámvasutak (állományvégjelig olvasás)

## A feladat leírása
Egy zsúfolt vidámparkban olykor több órát is sorban kell ahhoz állni, hogy felülhessünk egy-egy hullámvasútra. A parkok méretére és a kígyózó sorokra való tekintettel érdemes megtervezni, hogy milyen sorrendben ülünk fel a játékaikra. A [PortAventura World](https://www.portaventuraworld.com/en) Európa egyik legnagyobb vidámparkja, mely a Costa Braván, Salou és Tarragona között található. Klasszikus területe (a kontinens egyetlen Ferrari parkján kívül) több tematikus világot tartalmaz, amelyek mindegyikében található legalább egy hullámvasút.

Ebben a feladatban hullámvasutak adatait kell beolvasnod a standard inputról, rendezni, majd kiírni a standard outputra.

## Formátumok

* A standard bemeneten egy hullámvasút a következő formátumban szerepel:
    ```
    <hullámvasút_neve>;<világ_neve>;<legkisebb_magasság>;<várakozási_idő>
    ```

* A standard kimeneten egy hullámvasút a következő formátumban szerepel:
    ```
    <hullámvasút_neve> (<világ_neve>): <várakozási_idő>
    ```

* A jelölések:
  * `hullámvasút_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `világ_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `legkisebb_magasság`: egy nemnegatív egész érték
  * `várakozási_idő`: egy nemnegatív egész érték

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `RollerCoaster` típus
Definiáld a `RollerCoaster` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `name`: a hullámvasút neve (típus: `<class 'str'>`)
* `world`: a világ neve (típus: `<class 'str'>`)
* `height`: a legkisebb magasság (típus: `<class 'int'>`)
* `time`: a várakozási idő (típus: `<class 'int'>`)

## A(z) `line_to_coaster` függvény
Írj egy `line_to_coaster` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `RollerCoaster` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `RollerCoaster` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `RollerCoaster` rekord

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `"Furius baco;Polynesia;140;120"` | `RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120)` |
| `"Shambhala;China;140;120"` | `RollerCoaster(name='Shambhala', world='China', height=140, time=120)` |
| `"Dragon Khan;China;140;80"` | `RollerCoaster(name='Dragon Khan', world='China', height=140, time=80)` |
| `"Stampida;Far West;120;20"` | `RollerCoaster(name='Stampida', world='Far West', height=120, time=20)` |
| `"Tami Tami;SesamoAventura;100;20"` | `RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20)` |
| `"El Diablo;Mexico;140;30"` | `RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)` |

## A(z) `coaster_to_line` függvény

Írj egy `coaster_to_line` nevű függvényt, mely megkap egy `RollerCoaster` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `coaster` - a(z) `RollerCoaster` típusú rekord

### Visszaadott érték

* az `coaster` paraméternek megfelelő sztring reprezentáció

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `RollerCoaster(name='Stampida', world='Far West', height=120, time=20)` | `"Stampida (Far West): 20"`
| `RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20)` | `"Tami Tami (SesamoAventura): 20"`
| `RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)` | `"El Diablo (Mexico): 30"`
| `RollerCoaster(name='Dragon Khan', world='China', height=140, time=80)` | `"Dragon Khan (China): 80"`
| `RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120)` | `"Furius baco (Polynesia): 120"`
| `RollerCoaster(name='Shambhala', world='China', height=140, time=120)` | `"Shambhala (China): 120"`

## A(z) `sort_coasters` függvény

Írj egy `sort_coasters` nevű függvényt, mely megkap egy `RollerCoaster` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `coasters` - a(z) `RollerCoaster` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `coasters` lista a következő szempontok szerint rendezve:

	1. a várakozási idő szerint növekvő sorrend
	1. a legkisebb magasság szerint csökkenő sorrend
	1. a hullámvasút neve szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120), RollerCoaster(name='Shambhala', world='China', height=140, time=120), RollerCoaster(name='Dragon Khan', world='China', height=140, time=80), RollerCoaster(name='Stampida', world='Far West', height=120, time=20), RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20), RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)]` | `[RollerCoaster(name='Stampida', world='Far West', height=120, time=20), RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20), RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30), RollerCoaster(name='Dragon Khan', world='China', height=140, time=80), RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120), RollerCoaster(name='Shambhala', world='China', height=140, time=120)]` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `RollerCoaster` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. a(z) `RollerCoaster` lista előállítása a(z) `line_to_coaster()` függvény felhasználásával
	1. a(z) `RollerCoaster` lista rendezése a(z) `sort_coasters()` függvénnyel
	1. a(z) `RollerCoaster` lista kiírása a(z) `coaster_to_line()` függvény felhasználásával

## Megjegyzés a *C* nyelvű megoldásokhoz

* A rendezéshez a `qsort()` függvényt használd.
* A(z) `coaster_to_line()` függvény a `qsort()` függvény negyedik paramétereként megadható, összehasonlító függvény.
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
Furius baco;Polynesia;140;120
Shambhala;China;140;120
Dragon Khan;China;140;80
Stampida;Far West;120;20
Tami Tami;SesamoAventura;100;20
El Diablo;Mexico;140;30
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
Stampida (Far West): 20
Tami Tami (SesamoAventura): 20
El Diablo (Mexico): 30
Dragon Khan (China): 80
Furius baco (Polynesia): 120
Shambhala (China): 120
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
D;I;177;13
K;E;103;200
F;V;159;70
L;L;120;13
O;O;119;123
B;K;77;29
E;U;86;213
P;T;96;229
H;D;177;195
J;S;113;122
M;Z;108;147
N;D;81;114
Q;J;108;46
G;H;178;101
I;C;64;77
R;T;50;202
C;H;140;256
A;F;139;117
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
D (I): 13
L (L): 13
B (K): 29
Q (J): 46
F (V): 70
I (C): 77
G (H): 101
N (D): 114
A (F): 117
J (S): 122
O (O): 123
M (Z): 147
H (D): 195
K (E): 200
R (T): 202
E (U): 213
P (T): 229
C (H): 256
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
D;R;99;204
B;I;79;198
J;A;164;162
A;O;160;206
H;F;52;140
Q;P;135;46
O;H;171;75
I;N;108;299
F;V;117;177
G;S;57;298
N;Q;66;257
E;M;92;220
K;T;139;145
P;B;57;14
R;C;52;107
M;Y;146;215
C;X;157;175
L;J;59;282
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
P (B): 14
Q (P): 46
O (H): 75
R (C): 107
H (F): 140
K (T): 145
J (A): 162
C (X): 175
F (V): 177
B (I): 198
D (R): 204
A (O): 206
M (Y): 215
E (M): 220
N (Q): 257
L (J): 282
G (S): 298
I (N): 299
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
L;W;142;204
A;S;175;64
J;U;60;154
F;A;155;268
H;O;105;53
I;S;151;169
M;E;158;70
O;C;173;60
P;O;70;240
N;H;164;261
B;Z;159;65
K;S;168;35
Q;U;180;290
E;L;109;70
C;E;169;236
G;L;124;64
R;G;129;5
D;E;142;247
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
R (G): 5
K (S): 35
H (O): 53
O (C): 60
A (S): 64
G (L): 64
B (Z): 65
M (E): 70
E (L): 70
J (U): 154
I (S): 169
L (W): 204
C (E): 236
P (O): 240
D (E): 247
N (H): 261
F (A): 268
Q (U): 290
```
