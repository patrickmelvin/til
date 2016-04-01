You can copy the contents of a file to the clipboard by piping the output of the `cat` command to `pbcopy`

```
~$ cat some/file/path | pbcopy
```

Since the cat command also accepts a splat operator, this can be used to copy the contents of several files at once:

```
~$ cat some/example/directory/* | pbcopy
```
