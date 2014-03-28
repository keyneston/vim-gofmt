vim-gofmt requires you to have the standard golang vim package installed. If
you are using pathogen that is as easy as:

```VimL
" Go stores the official vim plugin at $GOROOT/misc/vim/
call pathogen#infect('bundle/{}', $GOROOT . '/misc/{}')
call pathogen#helptags()
```

This requires that you define $GOROOT in your OS. You can figure out what your
$GOROOT should be set to by running `go env`

To configure automatic GoFmt on save:

```VimL
augroup golangfmt
    autocm FileType go autocmd! golangfmt BufWritePre <buffer> GoFmt
augroup END
```
