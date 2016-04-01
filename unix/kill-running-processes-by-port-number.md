This command takes a port number and kills and process running on it.

```bash
~$ sudo kill `sudo lsof -t -i:3000`
```

Here it will stop processes running on port 3000.

`lsof` retrieves a list of pids and `kill` kills them.
