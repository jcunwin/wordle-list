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

