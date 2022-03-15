# Hashes and symbols

Just like arrays, hashes allow you to store multiple values together.
However, while arrays store values with a numerical index, hashes store information using key-value pairs.
Each piece of information in the hash has a unique label, and you can use that label to access the value.

For example, to create a hash, you can use `Hash.new` or just `{}`:
```
my_hash = {
  'key_1' => 'value 1',
  'key_2' => 'value 2
}
```
This will result in a hash with two values, each one indexed with a key.
You can access a value with `my_hash['key_1'] # this prints out 'value_1'`

Instead of using a string as a key, `'key_1'` and `'key_2'` in the example above, you can use symbols, like this:
```
my_hash = {
  key_1: 'value 1',
  key_2: 'value 2'
}
```

If you use hashes this way instead, you would access the values using `:key_1` and `:key_2` instead:
```
my_hash[:key_1] # prints out 'value 1'
my_hash[:key_2] # prints out 'value 2'
```

[Click here to go back to the Ruby basics](../)

[Click here to go to the next chapter](../conditional_statements/)
