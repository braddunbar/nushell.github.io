---
title: dfr n-unique
categories: |
  dataframe
version: 0.88.0
dataframe: |
  Counts unique values.
usage: |
  Counts unique values.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for dataframe

<div class='command-title'>{{ $frontmatter.dataframe }}</div>

## Signature

```> dfr n-unique {flags} ```


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Counts unique values
```nu
> [1 1 2 2 3 3 4] | dfr into-df | dfr n-unique
╭───┬──────────────╮
│ # │ count_unique │
├───┼──────────────┤
│ 0 │            4 │
╰───┴──────────────╯

```

Creates a is n-unique expression from a column
```nu
> dfr col a | dfr n-unique

```


**Tips:** Dataframe commands were not shipped in the official binaries by default, you have to build it with `--features=dataframe` flag