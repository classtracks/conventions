# Conventions

The vast majority of our coding conventions are covered by ESLint, a linting (or code cleaning) tool.
On the command line, just run eslint . to check for any issues and then fix them.
The rest of our conventions, which are not enforceable by ESLint, are found here.

## Table of Contents

* [Abbreviations](#abbreviations)
* [Case](#case)
* [Components](#components)
* [CSS Property Order](#css-property-order)
* [Import Order](#import-order)
* [Spacing](#spacing)
* [Testing](#testing) (TODO)
* [Variable Naming](#variable-naming)
* [Variable Order](#variable-order)

## Abbreviations

### Why???

## Case

### Why???

## Components

Components should be made as small as possible for easy testing.

Every component should follow this pattern

* Its own file
* Its own CSS class
  * Or ID if its an entire page
* Associated scss file
* Associated test file

Example

* `/some-directory/ComponentName.jsx`
* `<div className="ComponentName"></div>`
  * Or `<div id="ComponentName"></div>`
* `/stylesheets/some-directory/_ComponentName.scss``
* `/test/some-directory/ComponentName.tests.js`

### Why?

This makes it clear what files, tests, styles relate to each other.

## CSS Property Order

### Why???

## Import Order

Imports should be made in the following order

1. NPM packages
1. Meteor packages
1. *--space--*
1. Collections (absolute import)
1. *--space--*
1. Methods / actions (absolute import)
1. *--space--*
1. Global components (absolute import)
1. Containers (relative import)
1. Components (relative import)

### Why?

External packages are first as a standard in many communities.

The rest is dictated by what is needed to load a page.

1. The page needs data (collections)
1. The page needs to be able to act on that data (methods / actions)
1. The page needs to be able to render that data (global components / containers / components)

## Spacing

2 spaces, never 4, never tabs.

Do not align characters by using more or less spaces.

Ternary (`a ? b : c`) should be multi line when it feels too long. But if that's long, consider breaking it up into earlier variables.

Within JSX, ternary operators should always be multiline. 

All JSX and HTML tags should be on their own line. Text should also be on its own line.

### Why???

## Testing

### Why???

## Variable Naming

Names should make sense and be logical.

Objects should be nouns.

Arrays should be pluralized.

Booleans should be adjectives.

* Booleans do not need words like *has* or *is* if they're an adjective (`if (pretty)` works as well as `if (isPretty)`)
* If involving a noun, then a boolean should add a verb or adjective (`showButton` is less confusing than `button`)

### Why???

## Variable Order

Variable declarations and object keys should be in the following order

1. IDs of anything (`_id`, `gameId`, etc)
1. General variables (in alphabetical order)
1. `aria` attributes
1. `data` attributes
1. non event functions
1. event handlers (`onChange`, `onClick`, etc)

### Why???
