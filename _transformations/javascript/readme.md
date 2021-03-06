---
id: javascript
label: JavaScript
title: JavaScript - Transformations
type: transform
description: "Transform an input to an output using JavaScript."
since: 2x
install: auto
---

<!-- Attention authors: Do not edit directly. Please add your changes to the appropriate source repository -->

{% include base.html %}

# JavaScript Transformation Service

Transform an input to an output using JavaScript. 

It expects the transformation rule to be read from a file which is stored under the `transform` folder. 
To organize the various transformations, one should use subfolders.

## Example

Let's assume we have received a string containing `foo bar baz` and we're looking for a length of the last word (`baz`).

transform/getValue.js:

```
(function(i) {
    var array = i.split(" ");
    return array[array.length - 1].length;
})(input)
```
