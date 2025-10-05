## question1
移动到第一行
10dd 

## question2
Press Ctrl+Z while in normal mode. That suspends Vim and drops you back to the shell (you can resume Vim later with fg).

## question3
In Vim, open a split with something like :vsplit newfile.txt (or :split newfile.txt) so both files show side by side in separate windows.

use Ctrl+W to switch between windows.

## question4
Select the lines (visual mode with V), then press > to indent right (or < to indent left). Alternatively, in normal mode run :>start,end where start,end are line numbers or marks.

## question5
 One handy feature I love is Vim’s built-in substitution with live preview: run :s/old/new/gc to step through each
  match interactively—Vim highlights the current match, and you can accept (y), skip (n), or quit (q). It’s a quick way
  to make targeted replacements without leaving the editor.