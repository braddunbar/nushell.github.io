---
title: random dice
categories: |
  random
version: 0.88.0
random: |
  Generate a random dice roll.
usage: |
  Generate a random dice roll.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for random

<div class='command-title'>{{ $frontmatter.random }}</div>

## Signature

```> random dice {flags} ```

## Flags

 -  `--dice, -d {int}`: The amount of dice being rolled
 -  `--sides, -s {int}`: The amount of sides a die has


## Input/output types:

| input   | output    |
| ------- | --------- |
| nothing | list\<any\> |

## Examples

Roll 1 dice with 6 sides each
```nu
> random dice

```

Roll 10 dice with 12 sides each
```nu
> random dice --dice 10 --sides 12

```
