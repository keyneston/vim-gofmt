To configure automatic GoFmt on save:

```VimL
augroup golangfmt
    autocm FileType go autocmd! golangfmt BufWritePre <buffer> GoFmt
augroup END
```
