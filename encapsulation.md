Encapsulation is used for two purposes.

One of the purposes is that the user of the interface doesn’t necessarily want to know how the insides of our class is working
and also the internal representation of the Object is not visible to the outside world.
So for instance, if we have a class Dog that has two values, `@name` and `@age`, and we want our dog to age by 1, we can encapsulate
that function defining a method that does that.

```
class Dog

  attr_reader :name
  attr_reader :age

  def initialize(name, age)
    @name = name
    @age = age
  end

  def age_my_dog
    @age += 1
  end
end
```

As can be seen, this also allows information hiding. The only way the outside world can access the Class's values is if we define 
attr_reader for both values, otherwise if we want to know the age of our dog and type in `dog.age` it would throw a "NoMethodError".



