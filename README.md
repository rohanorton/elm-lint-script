# Elm Lint Script

A script for making elm make output something that can be used by vim neomake.

Put elm-lint executable in your path somewhere and then create file
`.vim/autoload/neomake/makers/ft/elm.vim` with the following lines:

```vim
function! neomake#makers#ft#elm#EnabledMakers()
    return ['elm_make']
endfunction

function! neomake#makers#ft#elm#elm_make()
	return { 'exe': 'elm-lint', 'errorformat': '%f:%l:%c [%t] %m', }
endfunction
```
