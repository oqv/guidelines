# Structuring Meteor Application

## Meteor.methods

- names: `Agencies.getCurrent`,  `Agencies.getOneById`, `Agencies.getByMarketplaceId` 
- files:
  - methods: `app/server/methods/Agencies.coffee`
  - test: `app/tests/jasmine/server/integration/server/methods/AgenciesSpec.coffee`

## Collections and Publications

- collection names: 
  - `Agencies`
- publication names: 
  - `Agencies.current`
  - `Agencies.oneById`
  - `Agencies.byMarketplaceId`
- files: 
  - schemas: `app/both/collections/Agencies.coffee`
  - publications: `app/server/collections/Agencies.coffee`
  - test: `app/tests/jasmine/server/integration/server/collections/AgenciesSpec.coffee`

## Routes, Events, Helpers, and Tempates

- Use `*.tpl.jade` instead of `*.jade` with `template(name='*')` in it.

- route: `agency/1234567890/report` 
- route and template name: `agencyReport`
- files:
  - styles: `app/client/Agencies/agencyReport.sass`
  - template: `app/client/Agencies/agencyReport.tpl.jade`
  - route: `app/client/Agencies/agencyReport.coffee`
  - test: `app/tests/jasmine/client/integration/client/Agencies/agencyReportSpec.coffee`
  
## Controllers

- If name ends with `-er` it's probably a set of methods. (It's a smell)
- Name can be plural only if it uses list in the constructor `class @Agencies extends @Collection`.
- `class @FormatURL extends @Format` - file `**/lib/FormatURL.coffee`

- name: `class @Collection`
- file: `**/lib/super/Collection.coffee`
- test: `app/tests/jasmine/*/unit/**/lib/super/CollectionSpec.coffee`

## UI components

- Everything goes into packages (Sass, CSS, Jade partials, etc)

### Helpers, Events, Templates

- name: `UIButton` 
- files: 
  - styles: `app/packages/plentiful:ui-button/client/UIButton.sass`
  - template: `app/packages/plentiful:ui-button/client/UIButton.tpl.jade`
  - helpers (and events, routes): `app/packages/plentiful:ui-button/lib/UIButton.coffee` 
  - template test: `app/packages/plentiful:ui-button/tests/jasmine/client/integration/UIButtonSpec.coffee`

### Controllers

- name: `class @UIButton extends @UI`
- file: 
  - class: `app/packages/plentiful:ui-button/lib/UIButton.coffee` 
  - test: `app/packages/plentiful:ui-button/tests/jasmine/client/unit/UIButtonSpec.coffee`
