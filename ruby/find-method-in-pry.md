You can perform a grep-like search for a method in a pry session with the `find-method` function.

```ruby
pry(main)> find-method to_yaml
Gem::Specification#to_yaml
```

You can pass in a namespace to narrow down the search.

```ruby
pry(main)> find-method history Pry
Pry.history=
Pry.save_history
Pry.load_history
Pry.history
Pry#update_input_history
Pry::Config
Pry::Config#history
Pry::Config#history=
```

If you call `find-method` with the `-c` flag, it will grep the source code of each method. This can be used to find calls to other methods.

```ruby
pry(main)> find-method -c save_history Pry
Pry.save_history: def self.save_history
Pry
Pry#repl_epilogue: Pry.save_history if Pry.config.history.should_save && Pry.active_sessions == 0
```
