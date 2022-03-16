# What is OOP?

OOP stands for **O**bject **o**riented **p**rogramming.

It is a programming paradigm that organizes software design around data, bundled into classes, or instances of classes called objects, rather than functions and raw data processing.

## What does this mean?

Say, for example you have the following code:
```
def car_goes_vroom(car_make)
  if car_make != 'Stojadin'
    puts 'VROOOM!'
  else
    puts 'not vroom :('
  end
end

car_goes_vroom('BMW') # prints out 'VROOM!'
car_goes_vroom('Stojadin') # print outs 'not vroom :('
```

If you're using OOP, you could instead implement something along the following:

```
class Car
  def car_goes_vroom
    puts @car_message
  end
end

class BMW < Car
  def intialize(car_message:)
    @car_message = car_message
  end
end

class Stojadin < Car
  def intialize(car_message:)
    @car_message = car_message
  end
end

car_1 = BMW.new(car_message: 'VROOM!')
car_1.car_goes_vroom # prints out 'VROOM!'

car_2 = Stojadin.new(car_message: 'not vrooom :(')
car_2.car_goes_vroom # prints out 'not vroom :('
```

Much like the non-OOP implementation, it does the exact same thing, but in a more organized way, without you having to care about any logic the `car_goes_vroom` function would take, you instead implement the behaviour into the method (in this case a class method) of the class itself and rely on it to do what it's suppose to.
In this example, both the `BMW` and `Stojadin` class end up inheriting the `car_goes_vroom` method from the `Car` class, which allows instances of those classes to use it.
However, the different values being passed into the constructors of those classes, make the parent class, `Car` in this case, behave differently, when the `car_goes_vroom` method is called on those objects.

This all might seem a bit confusing at first, but it will all be cleared up in future chapters.

[Click here to go back to the Ruby OOP chapter](../)

[Click here to go to the next chapter](../classes/)
