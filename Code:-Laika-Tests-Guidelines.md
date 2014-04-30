This guide presents a collection of best-practices and coding conventions
for the [Laika][laika] testing framework for Meteor applications.

## Suite and Tests

### Names

1. Separate tests by suites. Something like: one to ten tests per suite.
2. One file per suite.
3. Use [[Titles|English: Title Guidelines]] for suite names.
4. Separate suite name parts with hyphens.
5. Capitalize the first letter of test name.

E.g. `app/tests/api/users.coffee`
```
suite 'API - Users', ->
  test 'Sign up', (done, server, client) ->
```
### Test Order

Order tests by method purpose:

1. **Create**: Methods create, add, or upload an object.
2. **Get**: Fetch an object or a collection of objects.
3. **Set**: Update, change, edit.  
4. **Delete**: Remove, destroy.
5. Other methods.

[laika]: http://arunoda.github.io/laika/