---
layout: api-command
language: Ruby
permalink: api/ruby/eq/
command: eq
related_commands:
    '&, and': and/
    '|, or': or/
    ne: ne/
---

# Command syntax #

{% apibody %}
value.eq(value[, value, ...]) &rarr; bool
{% endapibody %}

# Description #

Test if two or more values are equal.

__Example:__ See if a user's `role` field is set to `administrator`. 

```rb
r.table('users').get(1)['role'].eq('administrator').run(conn)
```

__Example:__ See if three variables contain equal values.

```rb
r.eq(a, b, c).run(conn)
```
