# Instance and class variables

You've seen already what instance variables are in the classes chapter.
To keep it simple, instance variables make a given value be owned by the instance and only that instance of a given class.

Class variables change things around and are available to all instances of a given class.

Instance variables are denoted with a single `@` symbol.
Class variable are denoted with a double `@@` symbol.

As an example, take the following definition of a class:
```
class Parent
  @@family_things = []  # Shared between class and subclasses
  @shared_things  = []  # Specific to this class

  def self.family_things
    @@family_things
  end

  def self.shared_things
    @shared_things
  end

  def initialize
    @my_things = []  # Just for me
  end

  def family_things
    self.class.family_things # this is the same as @@family_things
  end

  def shared_things
    self.class.shared_things # this is the same as @shared_things
  end
end

class Child < Parent
  @shared_things = []
end
```

And seeing it in action:
```
mama = Parent.new
papa = Parent.new
joey = Child.new
suzy = Child.new

# the << operator appends to a given Array object, initialized, in this case with [], in the class defintions above

Parent.family_things << :house
papa.family_things   << :vacuum
mama.shared_things   << :car
papa.shared_things   << :blender
papa.my_things       << :quadcopter
joey.my_things       << :bike
suzy.my_things       << :doll
joey.shared_things   << :puzzle
suzy.shared_things   << :blocks

Parent.family_things #=> prints [:house, :vacuum]
Child.family_things  #=> prints [:house, :vacuum]
papa.family_things   #=> prints [:house, :vacuum]
mama.family_things   #=> prints [:house, :vacuum]
joey.family_things   #=> prints [:house, :vacuum]
suzy.family_things   #=> prints [:house, :vacuum]

Parent.shared_things #=> prints [:car, :blender]
papa.shared_things   #=> prints [:car, :blender]
mama.shared_things   #=> prints [:car, :blender]
Child.shared_things  #=> prints [:puzzle, :blocks]  
joey.shared_things   #=> prints [:puzzle, :blocks]
suzy.shared_things   #=> prints [:puzzle, :blocks]

papa.my_things       #=> prints [:quadcopter]
mama.my_things       #=> prints []
joey.my_things       #=> prints [:bike]
suzy.my_things       #=> prints [:doll] 
```

From the example above, the difference between instance and class variables should be obvious.

Every member of the `Parent` class (both `Parent` and it's derived class `Child`) have the same value of `@@family_things`.
`papa` is the only one who ever gets assigned a `blender`, but since it's saved in  `@shared_things`, `mama` also has it.
However, `papa` is the only one who gets assigned a `quadcopter` and it is only his, since it's his value of `@my_things`.

The examples continue in this fashion, see if you can understand all of them!

[Click here to go back to the Ruby OOP chapter](../)

[Click here to go to the next chapter](../attribute_accessors/)
