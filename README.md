**This is deprecated. Please use [vim-go](https://github.com/fatih/vim-go)**

Features
========

* Works with multiple views of the same file
* Doesn't mess up the undo tree (undoing the previous change undoes the fmt
  with it)
* Clears the error list when gofmt succeeds
* Automatically hides/shows the error list

Requirements
============

vim-gofmt requires you to have the standard golang vim package installed. If
you are using pathogen that is as easy as:

```VimL
" Go stores the official vim plugin at $GOROOT/misc/vim/
call pathogen#infect('bundle/{}', $GOROOT . '/misc/{}')
call pathogen#helptags()
```

This requires that you define $GOROOT in your OS. You can figure out what your
$GOROOT should be set to by running `go env`

Configuration
=============

Run Once
--------
  
```VimL
:GoFmt
```

Run Automatically
-----------------

```VimL
augroup golangfmt
    autocm FileType go autocmd! golangfmt BufWritePre <buffer> GoFmt
augroup END
```
