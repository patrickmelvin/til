When in a pry session, you can view the source code of a method with the `show-source` command. You can also view the source code of the super method by passing the `-s` flag. You can view the super method's super method with `-ss`.

```ruby
[1] pry(main)> show-source -s example.method

def super_method
  puts "This is method's super method"
end

[2] pry(main)> show-source -ss example.method

def super_super_method
  puts "This is super_method's super method"
end

[3] pry(main)>
```
