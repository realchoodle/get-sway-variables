# README.md

`swayvars` is a small Bash script that contains `getswayvars()`, a function that
gathers the variables from your Sway configuration file using `sway --verbose
--validate` and places them into an associative array. If called directly from
the terminal, `swayvars` will output your Sway variables using `@A` parameter
transformation (see `man bash`). To use this program, redirect it's output to a
file, and `source` that file in another script.

`swayvars` only takes one argument: an optional prefix for every key in the
associative array. For example, `swayvars prefix_` would make every key start
with `prefix_`, so `["var"]="value"` becomes `["prefix_var"]="value"`. **By
default, the array `swayvars` generates is called `SWAYVARS`**. To change this,
copy the array into a new one with a better name.
