## Naming Conventions

- Use full words.
- Use singular noun for a object, e.g. `person`, `project`.
- Use plural noun for a collection of objects, e.g. `people`, `projects`.
- Use a verb for methods, e.g. `projects.set.name`, `projects.get`.

## Template Names

- Use camelCase.

```jade
template(name='templateName')
```

## Methods

-

```coffee
# Set Project Name

## Arguments

project =
  name: String # New name
  _id: String # Id of the project

## Returns

true # The new name has been set
false # There is an error

    Meteor.methods

      'project/set/name': (project) ->
        ...
```

## Files and Directories

### Names

```
app
└─┬ both                                  // Both client and server
  │ ├─┬ 1.first.model
  │ │ ├── 1.first.method.litcoffee        // The method for the first model
  │ │ ├── 2.another.method.litcoffee
  │ │ └── 3.helper.litcoffee
  │ ├── 2.another.model
  │ ├─┬ collections
  │ │ └── new.litcoffee                   // Collection declarations
  │ ├── helpers                           // Helpers for all methods
  │ ├── lib
  │ └── configuration.litcoffee           // Global defaults, constants
  ├─┬ server                              // Server only code
  │ ├── 1.first.method.litcoffee          // The first server method
  │ ├── 2.another.method.litcoffee
  │ └─┬ collections
  │   ├── permissions.litcoffee           // Insert, update, remove permissions
  │   └── publish.litcoffee               // Publish collections
  ├─┬ client                              // Client only
  │ ├─┬ 1.first.view                      // The first view
  │ │ ├── 1.first.view.styl
  │ │ ├── 2.another.view.jade.html
  │ │ ├── 3.layout.jade.html
  │ │ └── 4.partial.jade.html
  │ ├── 2.another.view                    // Templates and client methods
  │ ├─┬ collections
  │ │ └── subscribe.litcoffee             // Subscribe to collections
  │ ├── layouts                           // Layouts for all views
  │ ├── partials                          // Partials for all views
  │ └── spec                              // Markup and styling Specifications
  ├── private                             // Private static files
  ├── public                              // Public static files
  └─┬ tests
    ├ integration                         // Test suite for the first view
    │ ├── 1.first.view.coffee
    │ └── 2.another.view.coffee
    └ unit                                // Test suite for the first model
      ├── 1.first.model.coffee
      └── 2.another.model.coffee
```

### File Extensions

- `.litcoffee` - Literate CoffeeScript
- `.coffee` - Literate CoffeeScript
- `.js` - JavaScript
- `.jade.html` - Jade
- `.html` - Spacebars
- `.styl` - Stylus
- `.scss` - SCSS