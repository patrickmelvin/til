The `!!` command can be used to evaluate any variable as a boolean.

```ruby
irb(main):005:0> 3.0.class
=> Float
irb(main):006:0> !!3.0
=> true
irb(main):007:0> !!"A string"
(irb):7: warning: string literal in condition
=> true
irb(main):008:0> !!nil
=> false
irb(main):009:0> !!true
=> true
```
