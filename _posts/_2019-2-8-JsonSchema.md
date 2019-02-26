---
layout: post
title: JSON Schema validation with Java & Python
---

[JSON Schema](https://json-schema.org/) is a declarative language for describing and validating the format and structure of a JSON document.

# Defining a JSON Schema

Considering the following _JSON Object_ representing an animal: 

```json
{
  "id": 1,
  "name": "dog"
}
```

The correspoding _JSON Schema_ is:

```json
{
    "$schema": "https://json-schema.org/draft-04/schema",
    "title": "Animal API",
    "description": "An animal",
    "type": "object",
    "properties": {
        "id": {"type": "integer"},
        "name": {"type": "string"}
    },
    "required": ["id", "name"]
}
```

# Validating in Java


# Validating in Python

