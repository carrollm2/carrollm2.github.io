---
layout: post
title:      "Class Constants vs Class Variables"
date:       2019-11-25 01:35:16 +0000
permalink:  class_constants_vs_class_variables
---


Recently I have been doing my best to expand my skillset and learn more about software engineering. These past couple of weeks I have been reading constantly and working through numerous exercises involving object oriented programming in Ruby.

I started with the basics of creating a class type and then assigning that class type attributes and methods. Shortly after, I was introduced to a Class Constant. Upon my first introduction to a Class Constant, I didn't think too much about it other than it being a variable assigned a value inside the class type definition.

A short time after, I was introduced to Class Variables. Then confusion took over inside my brain! Seemed so similar to Class Constant? Are they not the same thing? After some digging, I found the key difference which I hope to demonstrate below.

One of the class types I coded was for Artist (musician). So I had the constructor take name as an argument. Then I wanted all instances of class type artist to collect the artist name in a class variable.

```
class Artist

  attr_accessor :name

  @@all = []

  def initialize(name)
    @name = name
    @@all << self.name
  end

  def self.all
    @@all
  end

end
```

To access the names of all the artists created, I could call Artist.all which calls the self.all method and returns the value of the class variable, @@all.

Here @@all can change states. The value starts as empty array and then as each artist is created, the artist's name is added to array.

In contrast, using a class constant instead of a class variable would be the way to go when you have a value involving a class in which you don't want the values to change after initialized. 

```
class Artist

  attr_accessor :name

  GENRE = "rock"

  def initialize(name)
    @name = name
  end

  def self.print_artists

     puts GENRE

  end

end
```

Above, I assumed I was never going to create an artist outside the genre of "rock". Therefore, a class constant name GENRE would work better. I can then access the GENRE variable in a class method, self.print_artists.

Hope this helps and this concept is now a little less confusing than it was for me at first.


