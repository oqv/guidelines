1. Avoid object name duplication in property names.

```
// Good
project = 
  name: 'The Project'

// Bad
project = 
  projectName: 'The Project'
```

2. [Rule] Avoid adjectives when possible.

```
// Good
amount: 100

// Bad
totalAmount: 100
```

3. Use plurals for collections.

```
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
bookList =  // Avoid *list*, *group*, and other ugly suffixes.
  [
    title: 'Remote'
    author:  // Avoid using singular for collections.
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

4. Respect acronyms. 

```
// Good
HTMLTemplate

// Bad
HtmlTemplate
```

5. Place adjectives before an noun in this order:

- General opinion
- Specific opinion
- Size
- Shape
- Age
- Color
- Nationality
- Material

```
// Good
smallBookCover
largePhoto

// Bad
photoLarge
bookCoverSmall
```

6. For functions place verbs before the noun.
```
// Good
getName
setName

//Bad
nameGet
nameSet
```

7. Use the same verb for similar actions:
```// Good
setName

// Okay (not recommended)
rename

// Bad
changeName
```

*Recommended verbs*
Update - change many properties of the object
Create - create an object, insert in to the collection
Delete - remove an object from the collection
Set - change one property of the object
Unset - remove the property from the object
Get - read the object or its property

8. Use `is` in front of boolean field names.

```
// Good
isActive

// Bad
active
activated
```

9. Use *At* or *In* suffixes for date and time.

```
// Good
modifiedAt: '2014-06-03T13:47:30+00:00'  // Date ISO 8601
expiresIn: 123098 // Milliseconds from the moment
expiresAt: '2014-06-03T13:47:30+00:00'

//Bad
modified: '2014-06-03T13:47:30+00:00'
```

10. Use full words when possible

```
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
longitude
```