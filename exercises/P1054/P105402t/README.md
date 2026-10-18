# `P105402t` - Email címek (végjelig olvasás)

## A függvény
Írj egy `is_email_address` nevű függvényt, mely visszaadja azt, hogy a paramétereként megkapott sztring szabályos email cím-e!

### Magyarázat
Egy sztringet szabályos email címnek tekintünk, ha

1. csak betű, számjegy, `'-'` (mínuszjel), `'@'` (kukac) és `'.'` (pont) karaktereket tartalmaz,
1. pontosan egy darab `'@'` (kukac) karaktert tartalmaz,
1. a `'@'` (kukac) karakter nem a legelső és nem is a legutolsó karakter a sztringben,
1. a `'@'` (kukac) karakter mögötti rész legalább egy `'.'` (pont) karaktert tartalmaz,
1. a `'@'` (kukac) karakter utáni részben minden `'.'` (pont) karaktert megelőz legalább egy karakter, amely nem `'.'` (pont) és nem is `'@'` (kukac), és
1. az utolsó `'.'` (pont) karakter utáni részsztring legalább 2 karakter hosszúságú.

### Paraméterlista
1. `value` - az ellenőrizendő sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az ellenőrzés eredménye (`True`, ha a sztring megfelel a formátumnak, `False`, ha nem)

### Példák
 | `value` | Visszaadott érték |
 | :--- | --- |
 | `"user@company.com"` | `True` |
 | `"-@-.--"` | `True` |
 | `"where-is-the-end@"` | `False` |
 | `"user@nodot"` | `False` |
 | `"user@twodots..com"` | `False` |
 | `"user@short-domain.x"` | `False` |

## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét egy üres sor (`""`) jelzi (melyet már nem kell feldolgozni).
* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`value`) szerepel.
* A(z) `"YES"` sztring kerüljön a kimenetre, ha a függvény igaz (`True`) értéket ad vissza.
* A(z) `"NO"` sztring kerüljön a kimenetre, ha a függvény hamis (`False`) értéket ad vissza.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
user@company.com
-@-.--
where-is-the-end@
user@nodot
user@twodots..com
user@short-domain.x
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
YES
YES
NO
NO
NO
NO
```
