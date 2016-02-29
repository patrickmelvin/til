You can specify the language highlighting that you want to apply to a code snippet in markdown by following the code snippet tags with your language of choice.

```ruby
 `` `
   def foo
     return bar
   end
 `` `
```

This syntax highlighting works on github, which uses the linguist markdown parser. This parser has syntax highlighting for languages specified in [this languages.yml file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml). Among these are

* CSS
* CoffeeScript
* Diff
* JSON
* JavaScript
* Ruby
* SCSS
* SQL
* VIM
* YAML
