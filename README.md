codex
=====

> Good and bad practices from life experience.

# Content:

1. [Introduction](#Introduction) — few words about the Codex.
2. [Naming](#Naming) — a section about naming stuff.

# Introduction

`codex` is a handbook about code, architecture and things in-between.

Want to contribute? Read the short [guide](CONTRIBUTING.md) before you do.

# Naming

Some examples of odd and __bad__ class naming from one project:

```js
/*
`RichComboBoxComboBox` is a class, that represents `ComboBox` DOM element.
*/
class RichComboBoxComboBox extends ComboBox { /* ... */ }

/*
`RichComboBox` is a class, that represents form input with validation
and other logic.
*/
class RichComboBox extends CompositeFormInputEl {
  constructor() {
    // Composition: `RichComboBoxComboBox` inside `RichComboBox` to control the
    // visual representation with client logic.
    this.comboBox = new RichComboBoxComboBox();
  }

/*
Later, class was renamed `RichComboBoxComboBox` -> `LoaderComboBox`,
because it uses lazy loading, provided by `Loader`.
*/
```

```js
/*
View (representation, DOM element) of `FormOptionSet` for items of type `Options`.
*/
class FormOptionSetOptionView extends FormItemView { /* ... */ }
```
