# Elm Lint Script

A script for making elm make output something that can be used by vim neomake.

Put elm-lint executable in your path somewhere and add the following lines to
your `.vimrc` file:

```vim
let g:neomake_elm_elm_lint_maker = { 'exe': 'elm-lint', 'errorformat': '%f:%l:%c [%t] %m' }
let g:neomake_elm_enabled_makers = ['elm_lint']
```
