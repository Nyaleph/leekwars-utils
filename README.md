# Leekwars Utils library

This repository is meant as a collection of useful functions and classes to use
in your own AIs. They are meant to be quality of life enhancements and not as
a full ai.

## Content

At the moment only a few files are available but more is being worked on:

### Logger

Log important info. For that, there are currently a few methods available:

```js
logger.set_level(level) // Sets the logger level
logger.log_msg(level, category, message, color) // Displays a message in a certain color formatted using the log_message string
logger.save_ops(category) // Saved the ops cost of a certain category
logger.log_ops(level, category, color, overwrite) // Logs the operation cost since the last save_ops of a category and saves the new operation cost if overwrite is set to true
logger.log_cells(level, cells, color, is_index) // Marks the cells in a list. If is_index is false, it will mark the cells matching the key and not the value
```

### Color

A set of color, with an easy check to find the right color

```js
color.set(value, r, g, b) // Sets a color
color.get(value) // Gets a color
color.test_colors() // prints the name of each color in their corresponding color in order to check lisibility
```

### String

A list of useful functions for strings

```js
String.format(str, values) // Replaces every ${key} by the value matching the key in the table values
```

### Array

The arrayX functions reimplemented to have the callback use the key and array of the table.

```js
Array.fill(arr, callback, amount) // Returns an array filled with each result of the callback with numbers from 0 to amount - 1 as input
Array.map(arr, callback) // maps the array using callback
Array.forEach(arr, callback) // Applies the callback for each element of the array
Array.fold(arr, callback, first) // folds left the array
Array.filter(arr, predicate) // Filters the array of all the elements that doesn't match the predicate
```
