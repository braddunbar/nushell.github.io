---
title: into value
categories: |
  filters
version: 0.88.0
filters: |
  Infer nushell datatype for each cell.
usage: |
  Infer nushell datatype for each cell.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> into value {flags} ```

## Flags

 -  `--columns, -c {table}`: list of columns to update


## Input/output types:

| input | output |
| ----- | ------ |
| table | table  |

## Examples

Infer Nushell values for each cell.
```nu
> $table | into value

```

Infer Nushell values for each cell in the given columns.
```nu
> $table | into value -c [column1, column5]

```
