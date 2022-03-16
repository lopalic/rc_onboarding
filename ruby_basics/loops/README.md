# Loops and iterators

Apart from the `while` and `unless` loops you saw in the previous chapter, you can also loop/iterate through any kind of collection we've mentioned previously.
**But what are collections???** you might ask youself, and the answer to that is Arrays and Hashes, of course(or to put it more blunly, anything that has multiple values in it that you can iterate over).

Say, for example, you have the `[1, 2, 3]` array and you wanted to loop/iterate over it and print every value, you could do something like this:
```
[1, 2, 3].each do |value|
  puts value
end
```
Here, `value` is the iterator going through each and every element in the `[1, 2, 3]` array and accessing the value of that element of the array.

Similarly, if you had say a hash like this `{ a: 1, b: 2, c: 3}` and you wanted to loop/iterate over it and print its keys and values, you could do this:
```
{ a: 1, b: 2, c: 3}.each do |key, value|
  puts "hash on key: #{key} has the value: #{value}"
end
```
This would print out:
```
"hash on key: a has the value: 1"
"hash on key: b has the value: 2"
"hash on key: c has the value: 3"

```

This is a bit different from unsing just `value` in the case of arrays, but the general idea is that you put everything a given element has into an iterating variable.
So for a couple of examples:
`[1, 2, 3]` would only need a single iterator, in this example, called `value` to iterate over the values.
`{ a: 1, b: 2, c: 3}` needs two iterators, one for the keys and the other for the values to iterate over both of them.

You can try out the example involving hashes by running `ruby example` from this directory!

[Click here to go back to the Ruby basics chapter](../)

[Click here to go to the next chapter](../functions/)
