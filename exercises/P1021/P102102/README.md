# `P102102` - Aritmetikai műveletek #2

Írjon programot, amely a standard bemenetről egész számokat és a Python programozási nyelv operátorait olvassa soronként, majd a beolvasott értékeken elvégzi az operátor által jelzett műveletet, és a standard kimenetre írja az eredményt!

## A bemenet specifikációja

A bemenet sorainak mindegyike egy-egy tesztesetet ír le állományvégjelig (`EOF`). Minden teszteset egy `x op y` formátumú sor, ahol `x` és `y` egész számok, míg `op` a Python programozási nyelv egész típusú operandusokra alkalmazható alábbi aritmetikai operátorainak egyike: `+`, `-`, `*`, `/`, `//`, `%`. Az operandusok az operátortól egy-egy szóközzel vannak elválasztva.

## Megjegyzés `C` nyelvhez

A `//` operátor nem tárolható karakterként, ezért helyette használd a `'~'` karaktert.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
5 + -5
165 - -10
-5 * -2
23 / 8
23 // 8
25 % 3
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
0
175
10
2.875
2
1
```
