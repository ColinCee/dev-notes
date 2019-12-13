# CSS
Everything to do with css can go Here

## Selectors

Css can be a bit tricky to use with all the variety of selectors you can use. Here is a bunch of most common ones to get started.

### id
- #myElementId

### class
- .myClass

### element type
- input

Element types are the simplest in that they require nothing but the element itself for the selector
### children
- .parentClass > .childClass

Highly useful to when you wish to specify something more specific and an id is unavailable

### String operations

Say we have an id for an element that is in the format **alpha-x** where **x** is a random number. How do we go about selecting this id if we don't know the full string? Easy!


*Note*: id below can be substituted for any other attribute
#### starts with
- [id^=alpha]

#### contains
- [id*=ha]

#### ends with
- [id$=x]
