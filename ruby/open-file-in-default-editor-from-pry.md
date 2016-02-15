You can open a file from a pry instance in your default text editor with the edit command.

```ruby
pry(main)> edit -c
```

The `-c` flag can be used to open the currently opened file in the pry instance, or a filepath can be passed as a parameter to open another file. Alternatively, it can be used to edit a method with `edit Class#method` or `edit Class.method`.

`--in 1..2` can be used to open a line range from the pry buffer
`--ex` can be used to open the relevant file from the last exception (or `--ex N` to open the Nth file from the backtrace)
`-n` will prevent pry from reloading the file’s contents
`-r` will force pry to reload and eval files which do not end with .rb
