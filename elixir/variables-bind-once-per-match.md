Variables only bind once in a single match operator. That means that, although you can overwrite a variable bind in two subsequent matches, you cannot match a value to a variable and then match another value to that same variable in a single match.

```elixir
iex(1)> a = 1
1

iex(2)> a = 2
2

iex(3)> [a,a] = [1,1]
[1,1]

iex(4)> [a,a] = [1,2]
** (MatchError) no match of right hand side value: [1, 2]
```
