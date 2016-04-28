# InDRe
Insane Data Representation

## Definition
* Everything is a list.
* Every list item is a string of characters.
* There is no type of value. A value need to be parsed from a string of characters, with its type defined in somewhere else not within this scope.
* There are multiple delimeters, only limitted by the number of unique characters.
* Every literal follows an escape character. A pair of escape characters make a literal character.

## Example
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
