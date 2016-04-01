You can do a recursive grep for a terms, leaving out any logs with the command

```bash
~$ grep -r --exclude="*.log" _[search term]_ .
```

If there are any other fielname patterns that you want to exclude from the grep, you can just change the `*.log` or add another `--exclude` after the first.
