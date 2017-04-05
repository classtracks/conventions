# Conventions

The vast majority of our coding conventions are covered by ESLint, a linting (or code cleaning) tool.
On the command line, just run eslint . to check for any issues and then fix them.
The rest of our conventions, which are not enforceable by ESLint, are found here.

## Table of Contents

* [Abbreviations](#abbreviations)
  * [Accepted Abbreviations](#accepted-abbreviations)
* [Case](#case)
* [Components](#components)
* [CSS Property Order](#css-property-order)
* [Import Order](#import-order)
* [Spacing](#spacing)
* [Testing](#testing) (TODO)
* [Variable Naming](#variable-naming)
* [Variable Order](#variable-order)

## Abbreviations

Abbreviations should almost never be used with a few exceptions.

Ideally any abbreviation should be

* Commonly accepted
* Just a shortening of another word
* Significantly shorter than the original word
* Easily pronounceable
* Not easily confused with another word
* Middle letters, especially vowels, should not be removed

### Accepted Abbreviations

* alt - alternate
* auth - authorization
* id - identification
* nav - navigation
* pub - publication
* sub - subscription
* temp - temporary

### Why?

Because we write code for humans, not for machines.

Also, everything gets minimized and uglified in production anyway, no need to do it early.

## Case

CSS classes should match the same case of the component (generally **UpperCamelCase**) or should be dash-case

Directories should be **dash-case**

Files should match the same case as what is being exported

* If nothing is being exported, the file name should be **snake_case**

Variables should be **lowerCamelCase**

* If a variable is a container or component, it should be **UpperCamelCase**

### Why?

**lowerCamelCase** variables, **snake_case** file names, and **dash-case** directories / CSS classes are standards in many communities.

**UpperCamelCase** for all things component related has become a standard in React and makes it easy for IDE autocomplete suggestions.

## Components

Components should be made as small as possible for easy testing.

Every component should follow this pattern

* Its own file
* Its own CSS class
* Associated scss file
* Associated test file

Example

* `/some-directory/ComponentName.jsx`
* `<div className="ComponentName"></div>`
* `/stylesheets/some-directory/_ComponentName.scss``
* `/test/some-directory/ComponentName.tests.js`

### Why?

This makes it clear what files, tests, styles relate to each other.

## CSS Property Order

Comments and line breaks shown below not necessary in actual files.

```
.selector {
  /* Positioning */
  position: absolute;
  z-index: 10;
  top: 0;
  right: 0;

  /* Display & Box Model */
  display: inline-block;
  overflow: hidden;
  box-sizing: border-box;
  width: 100px;
  height: 100px;
  padding: 10px;
  border: 10px solid #333;
  margin: 10px;

  /* Color */
  background: #000;
  color: #fff;
  opacity: .5;

  /* Text */
  font-family: sans-serif;
  font-size: 16px;
  line-height: 1.4;
  text-align: right;

  /* Other */
  cursor: pointer;

  /* Transitions & Animations */
  transition: all 1s;
  animation: 3s slidein;
}
```

### Why?

Some components may end up having dozens of individual CSS property rules.
Lets try to make it easier to quickly scan a component's style declarations and understand how it is intended to look and behave.

Our convention is "grouped-by-type", based on [this CSS Tricks post.](https://css-tricks.com/poll-results-how-do-you-order-your-css-properties/)

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
1. Containers (relative import if in the same module)
1. Components (relative import if in the same module)

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
