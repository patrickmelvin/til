ActiveSupport provides a Hash class which does not distinguish between string and symbol keys. Hashes can be converted to this class with `#with_indifferent_access`.

```ruby
irb(main):001:0> hash = HashWithIndifferentAccess.new
=> {}
irb(main):002:0> hash[:foo] = 'bar'
=> { :foo => bar }
irb(main):003:0> hash[:foo]
=> 'bar'
irb(main):004:0> hash['foo']
=> 'bar'
irb(main):005:0> hash = { foo: 'bar' }
=> {}
irb(main):006:0> hash = hash.with_indifferent_access
=> { :foo => bar }
irb(main):007:0> hash[:foo]
=> 'bar'
irb(main):008:0> hash['foo']
=> 'bar'
```
