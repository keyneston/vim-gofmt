To configure automatic GoFmt on save:

    augroup golangfmt
	    autocm FileType go autocmd! golangfmt BufWritePre <buffer> GoFmt
	augroup END
