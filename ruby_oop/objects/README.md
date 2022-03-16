# Objects

We've already touched on the topic of objects without actually mentioning them, but put simply, objects, or instances, are unique occurences of a given class, each independant of the other.

Building on the example of dandelions from the chapter before, say you have the following code:
```
my_plant_1 = Dandelion.new()
my_plant_2 = Dandelion.new()
```

This would end up creating two separate objects, or instances, of the `Dandelion` class.
When the `new` method is called, in Ruby, the `intialize` method is called implicitly, this is what's called a constructor, which creates the object for you.

Following the code above and examples for before, let's say you have the following code:
```
my_plant_1.grow # would print out 'I grew 1 centimeter!'
my_plant_1.grow # would print out 'I grew 1 centimeter!'
my_plant_1.grow # would print out 'I grew 1 centimeter!'

my_plant_1.size # would return 3, at this point
my_plant_2.size # would return 0, at this point

# say our second plant keeps growing abnormally and the following line is caled 100 times
my_plant_2.grow # would print out 'I grew 1 centimeter!'

my_plant_1.introduce_myself # would print out "Hello! I'm a plant of the dandelion species, and I'm 3 centimeters tall!"
my_plant_2.introduce_myself # would print out "Hello! I'm a plant of the dandelion species, and I'm 100 centimeters tall!"

# uh-oh, a 100 centimeter tall dandelion seems pretty unlikely, let's prevent it from growing more before this gets out of hand!

my_plant_2.wilt # would print out 'I wilted.'

my_plant_2.introduce_myself # would, in this case, print out 'Sorry, but I appear to have wilted.'

# however, we're still happy with our first dandelion, and it's still alive!

my_plant_1.introduce_myself # would, in this case, print out 'Sorry, but I appear to have wilted.'
```

From this example, you can see that we made two instances of the `Dandelion` class, which are completely independant from each other.
One wilting away does not affect the other.

This is the same for all of the instances of `Dandelions` you would ever create, they would all have to `grow` on their own, and `wilt` on their own, without any other `Dandelion` caring much about the other.

[Click here to go back to the Ruby OOP chapter](../)

[Click here to go to the next chapter](../instance_and_class_methods/)
