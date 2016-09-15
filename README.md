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

## Case

## Components

## CSS Property Order

## Import Order

## Spacing

## Testing

2 spaces, never 4, never tabs.

Do not align characters by using more or less spaces.

Ternary (`a ? b : c`) should be multi line when it feels too long. But if that's long, consider breaking it up into earlier variables.

Within JSX, ternary operators should always be multiline. 

All JSX and HTML tags should be on their own line. Text should also be on its own line.

## Variable Naming

Names should make sense and be logical.

Objects should be nouns.

Arrays should be pluralized.

Booleans should be adjectives.

* Booleans do not need words like *has* or *is* if they're an adjective (`if (pretty)` works as well as `if (isPretty)`)
* If involving a noun, then a boolean should add a verb or adjective (`showButton` is less confusing than `button`)

## Variable Order

Variable declarations and object keys should be in the following order

1. IDs of anything (`_id`, `gameId`, etc)
1. General variables (in alphabetical order)
1. `aria` attributes
1. `data` attributes
1. non event functions
1. event handlers (`onChange`, `onClick`, etc)
