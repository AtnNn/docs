---
layout: api-command
language: Python
permalink: api/python/bracket/
command: '[] (bracket)'
related_commands:
    row: row/
    nth: nth/
    get_field: get_field/
---

# Command syntax #

{% apibody %}
sequence[attr] &rarr; sequence
singleSelection[attr] &rarr; value
object[attr] &rarr; value
array[index] &rarr; value
{% endapibody %}

# Description #

Get a single field from an object. If called on a sequence, gets that field from every object in the sequence, skipping objects that lack it.

__Example:__ What was Iron Man's first appearance in a comic?

```py
r.table('marvel').get('IronMan')['firstAppearance'].run(conn)
```

<!-- stop -->

The `[]` command also accepts integer arguments as array offsets, like the [nth](/api/python/nth) command.

__Example:__ Get the fourth element in a sequence. (The first element is position `0`, so the fourth element is position `3`.)

```py
r.expr([10, 20, 30, 40, 50])[3]

40
```
