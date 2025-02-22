---
title: seq date
categories: |
  generators
version: 0.88.0
generators: |
  Print sequences of dates.
usage: |
  Print sequences of dates.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for generators

<div class='command-title'>{{ $frontmatter.generators }}</div>

## Signature

```> seq date {flags} ```

## Flags

 -  `--output-format, -o {string}`: prints dates in this format (defaults to %Y-%m-%d)
 -  `--input-format, -i {string}`: give argument dates in this format (defaults to %Y-%m-%d)
 -  `--begin-date, -b {string}`: beginning date range
 -  `--end-date, -e {string}`: ending date
 -  `--increment, -n {int}`: increment dates by this number
 -  `--days, -d {int}`: number of days to print
 -  `--reverse, -r`: print dates in reverse


## Input/output types:

| input   | output       |
| ------- | ------------ |
| nothing | list\<string\> |

## Examples

print the next 10 days in YYYY-MM-DD format with newline separator
```nu
> seq date --days 10

```

print the previous 10 days in YYYY-MM-DD format with newline separator
```nu
> seq date --days 10 --reverse

```

print the previous 10 days starting today in MM/DD/YYYY format with newline separator
```nu
> seq date --days 10 -o '%m/%d/%Y' --reverse

```

print the first 10 days in January, 2020
```nu
> seq date --begin-date '2020-01-01' --end-date '2020-01-10'
╭───┬────────────╮
│ 0 │ 2020-01-01 │
│ 1 │ 2020-01-02 │
│ 2 │ 2020-01-03 │
│ 3 │ 2020-01-04 │
│ 4 │ 2020-01-05 │
│ 5 │ 2020-01-06 │
│ 6 │ 2020-01-07 │
│ 7 │ 2020-01-08 │
│ 8 │ 2020-01-09 │
│ 9 │ 2020-01-10 │
╰───┴────────────╯

```

print every fifth day between January 1st 2020 and January 31st 2020
```nu
> seq date --begin-date '2020-01-01' --end-date '2020-01-31' --increment 5
╭───┬────────────╮
│ 0 │ 2020-01-01 │
│ 1 │ 2020-01-06 │
│ 2 │ 2020-01-11 │
│ 3 │ 2020-01-16 │
│ 4 │ 2020-01-21 │
│ 5 │ 2020-01-26 │
│ 6 │ 2020-01-31 │
╰───┴────────────╯

```
