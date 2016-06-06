You can do a recursive grep for a term, leaving out any logs with the command

```bash
~$ grep -r --exclude="*.log" _[search term]_ .
```

If there are any other fielname patterns that you want to exclude from the grep, you can just change the `*.log` or add another `--exclude` after the first.

This can also be accomplished in ack with the `--ignore-file` flag:

``` bash
~$ ack --ignore-file=ext:log _[search term]_
```
