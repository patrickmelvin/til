The `presence_in` method from the ActiveSupport module can be used to check a value falls within a defined set of values. It will return the value if it exists within the set or nil if it does not. This can be used to sanitise user input, among other things.

```ruby
irb(main):001:0> 'words'.presence_in(%w(a set of words))
=> words
irb(main):002:0> 'utterances'.presence_in(%w(a set of words))
=> nil
```

This can be used as a shorter version of the more common

```ruby
if(%w(a set of words).include(value))
  value
else
  nil
end
```
