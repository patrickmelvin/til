You can run a command in all buffers by prepending it with `:bufdo`. For example:

```vim
:bufdo execute "normal! @a" | w
```

will run the macro bound to the character "a" in every buffer.

Therefore, if you wanted to run a find/replace on a directory, you could use

```
cd dir
vim *
:bufdo %s/old/new/g
```

and it will search for "old" in every buffer and replace it with "new".

As well as `:bufdo`, there are several other ways to group files you want to apply a command to.

| command | groups                     |
|---------|----------------------------|
| :tabdo  | all tabs                   |
| :windo  | all windows in current tab |
| :argo   | all files in argument list |
| :bufdo  | all buffers                |
