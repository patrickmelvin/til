This command can be used to strip trailing whitespace from the entire file

```vim
:%s/\s\+$//e
```

You can put it in your .vimrc file and set it to run:

- on saving the file
```vim
autocmd BufWritePre * | :%s/\s\+$//e
```

- on hitting <Ctrl-n>
```vim
nnoremap <silent> <C-n> :let _s=@/<Bar>:%s/\s\+$//e<Bar>:let @/=_s<Bar>:nohl<CR>
```
