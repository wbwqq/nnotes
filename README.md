# nnotes

nnotes is a command line note taking tool. The goal is to be able to add, view and manipulate notes quickly and easily.

[![asciicast](https://asciinema.org/a/EqqVnBPGQZgDo2PTTBg5Z6ynS.svg)](https://asciinema.org/a/EqqVnBPGQZgDo2PTTBg5Z6ynS)

## Installation

```bash
pip install nnotes
```

## Main commands help

Features:
- multiple notebooks
- add notes
- delete notes (single, multiple, range)
- create notebook
- delete notebook
- custom notebooks directory


```
Usage (nnotes can be launched by typing 'n' or 'nnotes'):
    n [command]
    nnotes [command]

Available commands:
    add [note]                                      add note to active notebook
    ls                                              list / view notes from active notebook
    rm [note num]                                   delete note numbered [note num]
    rm [note num1] [note num2] [note num3]          delete specified notes (however many specified)
    rm range [note num1] [note num2]                delete notes from [note num1] to [note num2] (included)
    
    add @[notebook] [note]                          add note [note] to notebook [notebook]
    ls @[notebook]                                  show notes from [notebook]
    rm @[notebook] [note num]                       delete note [note num] from [notebook]
    rm range @[notebook] [note num1] [note num2]    delete notes from [note num1] to [note num2] (included) from [notebook]

    add @[notebook]                                 create notebook [notebook]
    ls @                                            list all notebooks
    ls @ path                                       list notebooks with their path
    rm @[notebook]                                  delete notebook

    set active [notebook]                           set active notebook [notebook]
    get active                                      show active notebook

    get notebooks path                              show notebooks directory
    set notebooks path [notebooks path]             set notebooks directory

Examples:
    n add this is a note                            "this is a note" added to active notebook
    n add @todo go shopping                         "go shopping" added to "todo" notebook
    n rm 1                                          delete note 1 in active notebook
    n rm @todo 2 6 7                                delete notes 2, 6, 7 from "todo" notebook
```

### Note for Windows users:

Windows users must wrap arguments starting with @ with single or double quotes (ex. windows users should type `n ls '@'` instead of `n ls @` ), or escape commands starting with @ with a backtick (ex. ``n ls `@`` instead of `n ls @` )

 `n add '@school' new note` would be the way to add 'new note' to the 'school' notebook. Or alternatively:
 ``n add `@school new note`` would also work.

## Example usage

`n` and `nnotes` can both be used:
```bash
$ n add new note
```
is the same as:
```bash
$ nnotes add new note
```

Other example commands:

```bash
$ n ls
```

```bash
$ n add @main another note
```

```bash
$ n ls @
```
etc.