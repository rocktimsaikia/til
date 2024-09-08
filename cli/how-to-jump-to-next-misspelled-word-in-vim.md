# How to jump to next/previous misspelled words in Vim?

```sh
# Jump forwards to misspelled words
]s

# Jump backwards to misspelled words
[s

# Mark the word under cursor as correct
zg

# Mark the word under cursor as incorrect
zw
```

## How to list the spelling suggestions list in Vim?

Both the commands below opens the suggestions list from where you can select
the correct word for your misspelled word.

```sh
# in normal mode
z=

# in edit mode
ctrl + xs
```
