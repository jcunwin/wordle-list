# Example searches using grep

## Source

https://github.com/tabatkins/wordle-list

## Examples

```bash
curl -s ... | grep -v [dukfiht] | grep .r... | grep n | grep -v ...n. | grep g | grep -v ..g..
```

With downloaded `words.txt`:

```bash
cat words.txt | grep -v [rastclnehpp] | grep .i..o
```

E.g. 
- Eliminated letters: `grep -v [rastclnehpkb]
- Known letters in correct places: `grep .i..o`
- `o` not in position 2: `grep o | grep -v .o...`

```bash
cat words.txt | grep -v [rastclnehpkb] | grep .i..o | grep o | grep -v .o... | grep i | grep -v ..i.. | grep m | grep -v ..m..
```

E.g. "roast" got nothing. "cline" showed "e" green and "c" yellow.

```bash
cat words | grep -v [roastlin] | grep d...e | grep c | grep - v c....
```

Returned:

```
pecke
peece
emcee
educe
deuce
becke
```

Tried:

- SLATE - got L and E in wrong positions (no S, A or T)
- LEMON - got L, E, O in wrong positions (no M or N)
- HOLED - got H, O, E in correct positions, L wrong position, no D

```
cat words | grep -v [satmnd] | grep l | grep -v l.... | grep -v .l... | grep -v ..l.. | grep e | grep -v .e... | grep -v ....e | grep o | grep -v ...o. | grep ho.e.
```

Returned:
```
hovel
```
