You can return an empty activerecord relation with the `none` method. This can be useful in testing when you need to stub an activerecord search returning no results.

```ruby
irb(main):001:0> Tweets.none
=> #<ActiveRecord::Relation []>
```
