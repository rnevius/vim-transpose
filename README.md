# Vim Transpose

A WIP attempt at building a feature-complete clone of Emacs' transposing text feature.

## Roadmap

The relevant Emacs documentation for Transposing Text is provided here for reference:

### 16.2 Transposing Text

`C-t` – Transpose two characters (`transpose-chars`).

`M-t` – Transpose two words (`transpose-words`).

`C-M-t` – Transpose two balanced expressions (`transpose-sexps`).

`C-x C-t` – Transpose two lines (`transpose-lines`).

   The common error of transposing two characters can be fixed, when
they are adjacent, with the `C-t` command (`transpose-chars`).
Normally, `C-t` transposes the two characters on either side of point.
When given at the end of a line, rather than transposing the last
character of the line with the newline, which would be useless, `C-t`
transposes the last two characters on the line.  So, if you catch your
transposition error right away, you can fix it with just a `C-t`.  If
you don't catch it so fast, you must move the cursor back between the
two transposed characters before you type `C-t`.  If you transposed a
space with the last character of the word before it, the word motion
commands (`M-f`, `M-b`, etc.)  are a good way of getting there.
Otherwise, a reverse search (`C-r`) is often the best way.

   `M-t` transposes the word before point with the word after point
(`transpose-words`).  It moves point forward over a word, dragging the
word preceding or containing point forward as well.  The punctuation
characters between the words do not move.  For example, `FOO, BAR`
transposes into `BAR, FOO` rather than `BAR FOO,`.  When point is at the
end of the line, it will transpose the word before point with the first
word on the next line.

   `C-M-t` (`transpose-sexps`) is a similar command for transposing two
expressions (see Expressions in the docs), and `C-x C-t` (`transpose-lines`)
e
