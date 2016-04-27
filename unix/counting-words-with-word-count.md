The wd command can be used to count the number of words in a string parameter.

```bash
$ echo The quick brown fox jumps over the lazy dog | wc -w
$ 9
```

You can also pass the parameter from a file

```bash
$ wc -l < file1.txt
$ 14
```

You could use this to count the instances of a pattern in a directory.

```bash
$ grep -or pattern . | wc -l
$ 13
```

...or in a file

```bash
$ echo file2.txt | grep -o pattern | wc -l
```
