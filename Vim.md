# Vim

A quick cheatsheet for the vim commands I have Used

# Command Mode

## File management
- :w - Writes (save) existing file
- :q - Quits the Vim text editor
- :wq! - (force) Write and quit, useful for readonly files

## Manipulating text
- yy/Y - copy current line
- p - paste *after* current line
- P - paste *before* current line
- maa - mark the current line with a

### Deletion
- dd - deletes current line
- daw - delete the word under cursor
- caw - same as daw but places you into insert mode
- d'a - deletes from mark start to current line

### Navigation
- gg - jump to start of file
- $ - goes to end of line
- G - go to last line
- o - begin new line below current and switch to *insert* mode

### Visual Selection

This mode is useful for copy/pasting/deleting

- v - enter single character selection
- shift+v - enter line based selection
