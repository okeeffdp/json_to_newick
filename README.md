
# JSON to Newick

json_to_newick.py contains a function, json_to_newick, to convert a json object to newick format.

Parameters:
-----------
json - A JSON object. See [JSON].

Output:
-------
string - A string in Newick format. See [Newick format](http://en.wikipedia.org/wiki/Newick_format).

Example:
--------

```python
>>> json = {
	"name" : "F",
	"children": [
		{"name": "A", "branch_length": 0.1},
		{"name": "B", "branch_length": 0.2},
		{"name": "E","branch_length": 0.5,
		"children": [
			{"name": "C", "branch_length": 0.3},
			{"name": "D", "branch_length": 0.4}
			]
		}
		]
	}
>>> print(json_to_newick(json))
(A:0.1,B:0.2,(C:0.3,D:0.4)E:0.5)F;
```

By Daniel O'Keeffe

[JSON]: http://en.wikipedia.org/wiki/JSON