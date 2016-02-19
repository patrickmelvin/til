You can open a pry session from an irb instance. The practical use case of this is being given access to Pry commands, such as ls show-source and find-method.

```ruby
irb(main)> binding.pry
pry(main)>
```

```ruby
irb(main)> user = User.new
irb(main)> user.pry
pry(#<User>)>
```
