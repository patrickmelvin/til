An alternative to putting a `:path` statement in your gemfile is to point to a local gem with the `bundle config` command.

To take advantage of this feature, we first have to specify the remote repo and branch in the Gemfile.

```ruby
gem "localgem", github: "patrickmelvin/localgem", branch: "master"
```

You are then free to point to the local version of your gem with

```bash
bundle config local.localgem /path/to/localgem
```

To remove the local config once you don't need it:

```bash
bundle config --delete local.localgem
```
