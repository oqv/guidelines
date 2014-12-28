# Naming Conventions

This style guide includes recommendations for building JSON APIs in CoffeeScript syntax. In general, JSON APIs should follow the spec found at JSON.org. These guidelines are applicable to JSON requests and responses in APIs.

## Property Name Guidelines

### Property Name Format

- Property names should be meaningful names with defined semantics.
- Property names must be camel-cased, ASCII strings.
- The first character must be a letter, an underscore (_), or a dollar sign ($).
- Subsequent characters can be a letter, a digit, an underscore, or a dollar sign.
- Reserved JavaScript keywords should be avoided.


### Avoid object name duplication in property names

```coffeescript
// Good
project = 
  name: 'The Project'

// Bad
project = 
  projectName: 'The Project'
```

### Avoid adjectives when possible

```coffeescript
// Good
amount: 100

// Bad
totalAmount: 100
```

### Use plurals for collections

```coffeescript
// Good
books = 
  [
    title: 'Remote'
    authors: 
      [
        'Jason Fried'
        'David Heinemeier Hansson'
      ]
  ,
    title: 'Design Is a Job'
    authors:
      [
        'Mike Monteiro'
      ]
  ]

// Bad
bookList =  // Avoid *list*, *group*, and other ugly suffixes
  [
    title: 'Remote'
    author:  // Avoid using singular for collections
      [
        'Jason Fried'
        'David Heinemeier Hansson'
      ]
  ,
    title: 'Design Is a Job'
    author:
      [
        'Mike Monteiro'
      ]
  ]

```

### Respect acronyms

```coffeescript
// Good
HTMLTemplate

// Bad
HtmlTemplate
```

### Place adjectives before an noun in this order:

- General opinion
- Specific opinion
- Size
- Shape
- Age
- Color
- Nationality
- Material

```coffeescript
// Good
smallBookCover
largePhoto

// Bad
photoLarge
bookCoverSmall
```

### For functions place verbs before the noun

```coffeescript
// Good
getName
setName

//Bad
nameGet
nameSet
```

### Use the same verb for similar actions

```coffeescript
// Good
setName

// Okay (not recommended)
rename

// Bad
changeName
```

**Recommended verbs**

- Update - change many properties of the object
- Create - create an object, insert in to the collection
- Delete - remove an object from the collection
- Set - change one property of the object
- Unset - remove the property from the object
- Get - read the object or its property


### Use `is` prefix for boolean fields

```coffeescript
// Good
isActive

// Bad
active
activated
```

### Use `At` or `In` suffixes for date and time fields

```coffeescript
// Good
modifiedAt: '2014-06-03T13:47:30+00:00'  // Date ISO 8601
expiresIn: 123098 // Milliseconds from the moment
expiresAt: '2014-06-03T13:47:30+00:00'

//Bad
modified: '2014-06-03T13:47:30+00:00'
```

10. Use full words when possible

```coffeescript
// Good
latitude
longitude
maximum
maximalSize

// Okay (not recommended)
max
min

// Bad
lat
lng
```
