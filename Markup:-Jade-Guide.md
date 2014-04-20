# Jade Guide

## Single and Double Quotes

1. Always use single quotes.
2. Use double quotes inside single quotes only.

```jade
// Good
.input(value='{{session "name"}}')

// Bad
.input(value="{{session 'name'}}")
```

## Multiple Attributes

1. Add a new line right after opening bracket.
2. Separate attributes with new lines.
3. Keep closing bracket with the same line

```jade
// Good
input(
  data-action='create'
  type='text'
  placeholder='name')

// Bad
input(data-action='create', type='text', placeholder='name')

// Bad
input(data-action='create'
  type='text'
  placeholder='name')

// Bad
input(
  data-action='create'
  type='text'
  placeholder='name'
  )
```