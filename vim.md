# Vim Cheatsheet

## Vim Tutor

Access vim tutor via `vimtutor` and follow along with the instructions.

### Lesson 1 SUMMARY

1. The cursor is moved using either the arrow keys or the `hjkl` keys.
    - `h`: left
    - `j`: down
    - `k`: up
    - `l`: right
1. To start Vim from the shell prompt type:
    - `vim FILENAME <ENTER>`
1. To exit Vim:
    - `<ESC>   :q!   <ENTER>`: trash all changes
    - `<ESC>   :wq   <ENTER>`: save the changes
1. To delete the character at the cursor type:
    - `x`
1. To insert or append text type:
    - `i type inserted text <ESC>`: insert before the cursor
    - `A type appended text <ESC>`: append after the line
1. Pressing `<ESC>` will place you in Normal mode or will cancel an unwanted and partially completed command.

### Lesson 2 SUMMARY

1. To delete from the cursor up to the next word type:
    - `dw`
2. To delete from the cursor to the end of a line type:
    - `d$`
3. To delete a whole line type:
    - `dd`
4. To repeat a motion prepend it with a number:
    - `2w`
5. The format for a change command is:
    - `operator number motion`
    - where:
      - `operator`: is what to do, such as `d` for delete
      - `number`: is an optional count to repeat the motion
      - `motion`: moves over the text to operate on, such as `w` (word), `$` (to the end of line), etc.
6. To move to the start of the line use a zero:
    - `0`
7. Undo:
    - `u`: undo previous actions
    - `U`: undo all the changes on a line
    - `CTRL-R`: redo

### Lesson 3 SUMMARY

1. To put back text that has just been deleted, type `p`.  This puts the deleted text AFTER the cursor (if a line was deleted it will go on the line below the cursor).
2. To replace the character under the cursor, type `r` and then the character you want to have there.
3. The change operator allows you to change from the cursor to where the motion takes you.  eg. Type `ce` to change from the cursor to the end of the word, `c$` to change to the end of a line.
4. The format for change is:
    - `c number motion`
