You can use the `-c` flag to count the number of instances of your search term when searching with grep. The number will be appended to the end of the filename.

```bash
~$ grep -c words *
  1 test1.md:3
  2 test2.md:2
  3 test3.md:0
```

You can pipe this into another grep to further narrow down your search. Say you want to find files which have the pattern "words" twice:

```bash
~$ grep -c words * | grep ":2"
  1 test2.md:2
```
