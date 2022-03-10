# Classes

Classes are blueprints, or prototypes, or even more simply, a collection of definitions that define some sort of behaviour.

For example, take a look at the following class:
```
class Plant
  def initialize(species:)
    @species = species
    @size = 0
  end

  def grow
    @size += 1
    puts 'I grew 1 centimeneter!
  end

  def wilt
    @size = -1
    puts 'I wilted.'
  end

  def introduce_myself
    if @size >= 0
      puts "Hello! I'm a plant of the #{@species} species, and I'm #{size} centimeters tall!"
    else
      puts 'Sorry, but I appear to have wilted.'
    end
  end
end
```

To keep things simple, let's say you're describing how a dandelion behaves in its life-cycle:

```
my_plant = Plant.new(species: 'dandelion')

my_plant.grow # would print out 'I grew 1 centimeter!'
my_plant.grow # would print out 'I grew 1 centimeter!'
my_plant.grow # would print out 'I grew 1 centimeter!'

my_plant.size # would return 3, at this point

my_plant.introduce_myself # would print out "Hello! I'm a plant of the dandelion species, and I'm 3 centimeters tall!"

my_plant.wilt # would print out 'I wilted.'

my_plant.introduce_myself # would, in this case, print out 'Sorry, but I appear to have wilted.'

```

This would allow us to define a more specific class, say `Dandelion` which would look something along the lines of this:
```
class Dandelion < Plant
  def initialize
    super(species: 'Dandelion')
  end
end
```

What this does is pass the `'Dandelion'` value to the `@species` variable in the `Plant` class, creating the same result as we have in the example above, however, instead of using `Plant.new`, we would use `Dandelion.new`, without even specifying anything(since the `Dandelion` class creates a `Plant` with the arguments we want all by itself:
```
my_plant = Dandelion.new()

my_plant.grow # would print out 'I grew 1 centimeter!'
my_plant.grow # would print out 'I grew 1 centimeter!'
my_plant.grow # would print out 'I grew 1 centimeter!'

my_plant.size # would return 3, at this point

my_plant.introduce_myself # would print out "Hello! I'm a plant of the dandelion species, and I'm 3 centimeters tall!"

my_plant.wilt # would print out 'I wilted.'

my_plant.introduce_myself # would, in this case, print out 'Sorry, but I appear to have wilted.'
```

[Click here to go back to the Ruby OOP](../)

[Click here to go to the next chapter](../objects/)
