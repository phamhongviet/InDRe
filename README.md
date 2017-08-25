# InDRe
Insane Data Representation.         
The insanity of this is as high as its uselessness.

## Definition
* Everything is a list.
* Every list item is a list of characters (normal people call them strings).
* There is no type of value. A value need to be parsed from a string of characters, with its type defined in somewhere else not within this scope.
* There are multiple delimeters, only limitted by the number of unique characters.
* Every literal follows an escape character. A pair of escape characters make a literal character.

## Example
Max level of delimiters: 5

| effect | character |
|--------|-----------|
| escape | \ |
| delimiter 1 | new line (\n) |
| delimiter 2 | : |
| delimiter 3 | = |
| delimiter 4 | + |
| delimiter 5 | - |

## Conversion

```json
{
	"ListOne": [
		"i1",
		"i2",
		"i3"
	],
	"ListTwo": [
		"i4",
		"i5"
	],
	"Dict": {
		"this": "that",
		"these": "those"
	}
}
```

```indre
ListOne:i1=i2=i3
ListTwo:i4=i5
Dict:this+that=these+those
```

```yaml
---
keys:
- "ABC::DEF=5+3-2"
- "XYZ\0123"
locks:
- "dGhpcyBpcyBhd2Vzb21lCg=="
```

```indre
keys:ABC\:\:DEF\=5\+3\-2=XYZ\\0123
locks:dGhpcyBpcyBhd2Vzb21lCg\=\=
```
