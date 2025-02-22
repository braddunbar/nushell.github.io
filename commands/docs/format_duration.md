---
title: format duration
categories: |
  strings
version: 0.88.0
strings: |
  Outputs duration with a specified unit of time.
usage: |
  Outputs duration with a specified unit of time.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for strings

<div class='command-title'>{{ $frontmatter.strings }}</div>

## Signature

```> format duration {flags} (format value) ...rest```

## Parameters

 -  `format value`: the unit in which to display the duration
 -  `...rest`: For a data structure input, format duration at the given cell paths


## Input/output types:

| input          | output       |
| -------------- | ------------ |
| duration       | string       |
| list\<duration\> | list\<string\> |
| table          | table        |
## Examples

Convert µs duration to the requested second duration as a string
```nu
> 1000000µs | format duration sec
1 sec
```

Convert durations to µs duration as strings
```nu
> [1sec 2sec] | format duration µs
╭───┬────────────╮
│ 0 │ 1000000 µs │
│ 1 │ 2000000 µs │
╰───┴────────────╯

```

Convert duration to µs as a string if unit asked for was us
```nu
> 1sec | format duration us
1000000 µs
```
