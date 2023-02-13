# CSS Selectors Cheatsheet

Hi! This is a cheatsheet for CSS selectors. It is a part of the [CSS Tutorial](https://github.com/amulifts/css-tutorial) for everyone who wants to learn CSS.

## Element selectors

**Element** -- selects all `h2` elements on the page

```CSS
h2 {
    foo: bar;
}
```

- **Example** : - **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/1_element.html)

**Group** -- selects all `h1`, `h2` and `h3` elements on the page

```CSS
h1, h2, h3 {
    foo: bar;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/2_group.html)

## Class and ID selectors

**Class** -- selects all elements with class attribute containing `foo` or only `p` elements with that class

```CSS
.foo {
    bar: fum;
}
p.foo {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/3_class.html)

**ID** -- selects the element with 'foo' id attribute value

```CSS
#foo {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/4_id.html)

## Contextual selectors

**Descendant** -- selects all `p` elements within the infinite-level hierarchy of element `#foo` descendants

```CSS
#foo p {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/5_descendant.html)

**Adjacent sibling** -- selects the sibling element `p` that is immediately next to `h2` element

```CSS
h2 + p {
    foo: bar;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/6_adjacent_sibling.html)

**Child** -- selects all `p` elements that are immediate children of `#foo` element

```CSS
#foo > p {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/7_child.html)

**General sibling** -- selects all elements `p` that are siblings to the `h2` element

```CSS
h2 ~ p {
    foo: bar;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/8_general_sibling.html)

## Pseudo-class selectors

### Pseudo-class selectors for link and user states

**Unvisited link** -- applies to link elements that have not been visited

```CSS
a:link {
    foo: bar;
}
```

**Visited link** -- applies to link elements that have been visited

```CSS
a:visited {
    foo: bar;
}
```

**Focus state** -- applies to selected `.foo` element that is ready for input

```CSS
.foo:focus {
    bar: fum;
}
```

**Focus within state** -- applies to selected `.foo` element that is focused or has any focused child

```CSS
.foo:focus-within {
    bar: fum;
}
```

**Hover state** -- applies when mouse pointer is over the `.foo` element

```CSS
.foo:hover {
    bar: fum;
}
```

**Active state** -- applies when `.foo` element is in process of being clicked

```CSS
.foo:active {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/9_pseudo_class.html)

### Pseudo-class selectors that apply to siblings

**First child** -- selects the specified `.foo` element when it is the first child of its parent

```CSS
.foo:first-child {
    bar: fum;
}
```

**Last child** -- selects the specified `.foo` element when it is the last child of its parent

```CSS
.foo:last-child {
    bar: fum;
}
```

**Only child** -- selects the specified `.foo` element when it is the only child of its parent

```CSS
.foo:only-child {
    bar: fum;
}
```

**First of type** -- selects the `h2` element when it is the first element of its type within its parent element

```CSS
h2:first-of-type {
    foo: bar;
}
```

**Last of type** -- selects the `h2` element when it is the last element of its type within its parent element

```CSS
h2:last-of-type {
    foo: bar;
}
```

**Only of type** -- selects the `h2` element when it is the only element of its type within its parent element

```CSS
h2:only-of-type {
    foo: bar;
}
```

**Nth child** -- selects the `n`th `.foo` child element

```CSS
.foo:nth-child(n) {
    bar: fum;
}
```

**Nth last child** -- selects the `n`th `.foo` child element counting backwards

```CSS
.foo:nth-last-child(n) {
    bar: fum;
}
```

**Nth of type** -- selects the `n`th `h2` child element of its type

```CSS
h2:nth-of-type(n) {
    foo: bar;
}
```

**Nth last of type** -- selects the `n`th `h2` child element of its type counting backwards

```CSS
h2:nth-last-of-type(n) {
    foo: bar;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/10_pseudo_class.html)

Useful `n` values:

- `odd` or `2n+1` -- every odd child or element
- `even` or `2n` -- every even child or element
- `n` -- every nth child or element
- `3n` -- every third child or element (3, 6, 9, ...)
- `3n+1` -- every third child or element starting with `1` (1, 4, 7, ...)
- `n+6` -- all but first five children or elements (6, 7, 8, ...)
- `-n+5` -- only first five children or elements (1, 2, ..., 5)

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/11_using_n.html)

### Pseudo-element selectors

**First letter** -- selects the first letter of the specified `.foo` element, commonly used with `:first-child` to target first paragraph

```CSS
.foo::first-letter {
    bar: fum;
}
```

**First line** -- selects the first line of the specified `.foo` element, commonly used with `:first-child` to target first paragraph

```CSS
.foo::first-line {
    bar: fum;
}
```

**Before** -- adds generated content before the `.foo` element when used with `content` property

```CSS
.foo::before {
    bar: fum;
    content: 'baz';
}
```

**After** -- adds generated content after the `.foo` element when used with `content` property

```CSS
.foo::after {
    bar: fum;
    content: 'baz';
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/12_pseudo_elements.html)

## Attribute selectors

**Present** -- selects `.foo` elements with `bar` attribute present, regardless of its value

```CSS
.foo[bar] {
    fum: baz;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/13_attribute_present.html)

**Exact** -- selects `.foo` elements where the `bar` attribute has the exact value of `fum`

```CSS
.foo[bar="fum"] {
    baz: qux;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/14_attribute_exact.html)

**Whitespace separated** -- selects `.foo` elements with `bar` attribute values contain specified partial value of `fum` (whitespace separated)

```CSS
.foo[bar~="fum"] {
    baz: qux;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/15_attribute_whitespace_separated.html)

**Hyphen separated** -- selects `.foo` elements with `bar` attribute values contain specified partial value of `fum` immediately followed by hyphen (`-`) character

```CSS
.foo[bar|="fum"] {
    baz: qux;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/16_attribute_hyphen_separated.html)

**Begins with** -- selects `.foo` elements where the `bar` attribute begins with `fum`

```CSS
.foo[bar^="fum"] {
    baz: qux;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/17_attribute_begin_with.html)

**Ends with** -- selects `.foo` elements where the `bar` attribute ends with `fum`

```CSS
.foo[bar$="fum"] {
    baz: qux;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/18_attribute_end_with.html)

**Contains** -- selects `.foo` elements where the `bar` attribute contains string `fum` followed and preceded by any number of other characters

```CSS
.foo[bar*="fum"] {
    baz: qux;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/19_attribute_contains.html)

## Misc selectors

**Not** -- selects `.foo` elements that are NOT `.bar` elements

```CSS
.foo:not(.bar) {
    fum: baz;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/20_not_selector.html)

**Root** -- selects the highest level parent element in the DOM

```CSS
:root {
    foo: bar;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/21_root.html)

**Empty** -- selects `.foo` elements that have no children or whitespace inside

```CSS
.foo:empty {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/22_empty.html)

**In-range** and **Out-of-range** -- selects `.foo` elements that have values in or out of range

```CSS
.foo:in-range {
    bar: fum;
}
.foo:out-of-range {
    bar: fum;
}
```

- **Example** : [View the code](https://github.com/amulifts/css-tutorial/blob/main/main/bonus/23_range.html)
