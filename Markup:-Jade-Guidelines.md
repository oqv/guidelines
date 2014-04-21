This guide presents a collection of best-practices for the [Jade](http://jade-lang.com/). Jade is a node template engine.

## Code Layout

### Maximum Line Length

Limit all lines to a maximum of **79 characters**.

## Tag Attributes

### Single and Double Quotes

1. Always use single quotes.
2. Use double quotes inside single quotes only.

```jade
// Good
input(value='{{session "name"}}')

// Bad
input(value="{{session 'name'}}")
```

### Single Attribute

1. Keep an attribute in the same line with the tag.

```jade
// Good
input(type='text')

// Bad
input(
  type='text')
```

### Multiple Attributes

1. Add a new line right after the opening bracket.
2. Separate attributes with a new line.
3. Keep the closing bracket within the same line.

```jade
// Good
input(
  type='text'
  placeholder='name')

// Bad
input(type='text', placeholder='name')

// Bad
input(type='text'
  placeholder='name')

// Bad
input(
  type='text'
  placeholder='name'
  )
```

## Text

1. Keep a one-liner text in the same line with the tag.
2. If there are more than one tag attribute or if text doesn't fit into one line
then pipe the text.

```jade
// Good
.menu
  a.menu__item.active Home
  a.menu__item(href='/about') About

// Good
.button(
  data-action='save'
  disabled={{isSaveDisabled}}) 
    | Save

// Good
p.body
 | Tim earned an M.B.A. from Duke University, where he was a Fuqua Scholar, 
 | and a Bachelor of Science degree in Industrial Engineering from Auburn
 | University.

// Bad
.menu
  a.menu__item.active.
    Home
  a.menu__item(href='/about') 
    | About

// Bad (82 characters in one line)
p.body Tim earned an M.B.A. from Duke University, where he was a Fuqua Scholar...
```