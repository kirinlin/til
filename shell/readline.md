# readline

https://wiki.archlinux.org/title/Readline

files: `~/.inputrc` and `/etc/inputrc`

## How to list readline variables with their current value

https://unix.stackexchange.com/a/642392

```console
linkirin@m91p: ~$ bind -V
bind-tty-special-chars is set to `on'
blink-matching-paren is set to `off'
byte-oriented is set to `off'
colored-completion-prefix is set to `off'
colored-stats is set to `off'
completion-ignore-case is set to `off'
completion-map-case is set to `off'
convert-meta is set to `off'
disable-completion is set to `off'
echo-control-characters is set to `on'
enable-bracketed-paste is set to `off'
enable-keypad is set to `off'
enable-meta-key is set to `on'
expand-tilde is set to `off'
history-preserve-point is set to `off'
horizontal-scroll-mode is set to `off'
input-meta is set to `on'
mark-directories is set to `on'
mark-modified-lines is set to `off'
mark-symlinked-directories is set to `on'
match-hidden-files is set to `on'
menu-complete-display-prefix is set to `off'
meta-flag is set to `on'
output-meta is set to `on'
page-completions is set to `on'
prefer-visible-bell is set to `on'
print-completions-horizontally is set to `off'
revert-all-at-newline is set to `off'
show-all-if-ambiguous is set to `off'
show-all-if-unmodified is set to `off'
show-mode-in-prompt is set to `off'
skip-completed-text is set to `off'
visible-stats is set to `off'
bell-style is set to `audible'
comment-begin is set to `#'
completion-display-width is set to `-1'
completion-prefix-display-length is set to `0'
completion-query-items is set to `100'
editing-mode is set to `emacs'
emacs-mode-string is set to `@'
history-size is set to `0'
keymap is set to `emacs'
keyseq-timeout is set to `500'
vi-cmd-mode-string is set to `(cmd)'
vi-ins-mode-string is set to `(ins)'
```
