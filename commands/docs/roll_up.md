---
title: roll up
categories: |
  filters
version: 0.88.0
filters: |
  Roll table rows up.
usage: |
  Roll table rows up.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> roll up {flags} ```

## Flags

 -  `--by, -b {int}`: Number of rows to roll


## Input/output types:

| input | output |
| ----- | ------ |
| table | table  |

## Examples

Rolls rows up
```nu
> [[a b]; [1 2] [3 4] [5 6]] | roll up
╭───┬───┬───╮
│ # │ a │ b │
├───┼───┼───┤
│ 0 │ 3 │ 4 │
│ 1 │ 5 │ 6 │
│ 2 │ 1 │ 2 │
╰───┴───┴───╯

```


**Tips:** Command `roll up` was not included in the official binaries by default, you have to build it with `--features=extra` flag