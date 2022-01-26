---
layout: page
title: OOP
---

## Learning Goals

- Explain the core concepts of Object-Oriented Programming
- Gain exposure and familiarity with the Ruby syntax for classes and object instances

## Vocabulary

- attribute
- class
- initialize
- method
- object instance
- Object-Oriented Programming (OOP)

## What is OOP?

Back End Engineering is concerned with the management of data for an application. There are different ways we can structure the data itself as well as the systems that manage it. Object-Oriented Programming (OOP) is one way to design a program to manage the data in a Back End.

OOP is not exclusive to Ruby! In fact, many of the most widely used programming languages follow the patterns of OOP, including Java, C#, and Python.

## Connecting OOP to Real-World Scenarios

In the introduction, we shared that Object-Oriented Programming (OOP) is a paradigm for how we can organize code. Without seeing examples, that definition just feels… unhelpful. In this section, we won’t dig into code quite yet, but we’ll do some thinking and list-making to set ourselves up to write code in the next section!

### Car Factory

Let’s think about some components of a Ford car factory. We may make some stuff up, but this analogy should help us build context for what OOP is.
- The factory has a machine that is designed to make a Ford Escape
- All Escapes have four wheels and four doors
- The color, interior fabric and engine size can vary from one Escape to another

With the information above, in theory, the manager at the factory should be able to say “please make a blue Escape with a leather interior and 2.5 cylinder engine”, and that should be possible.

That example about the car factory ties directly to concepts of OOP. We will use three main technical terms today. They are below, with the connection to the car factory example:

- **`class`** - A class is like a blueprint or template. The factory machines are designed to make a car - that is the template for ALL Escapes. We could probably name it the EscapeCar class.
- **`object/instance`** - An instance is an object that is made from the class template. The blue Escape that the manager requested (and was able to physically sit in and drive) is referred to as an object or instance of the EscapeCar class.
- **`attribute`** - An attribute is a specific characteristic about an instance that has the potential of varying from other instances. With our Escapes, color, interior and engine would be attributes, because they weren’t programmed into the template, but were extra information the manager was able to give for each specific instance of that class.

### Classes and Objects - At Home!

Pick an object that you see sitting around in your home. It could be a candle, water bottle, glove, anything!

Brainstorm:
- What _type_ of object is it? What might the class name be?
- Are there multiple objects/instances of it in your home, or in the world? List a few.
- What are some of its attributes?

## How to CODE these concepts

### Explore Class Syntax

While this may feel uncomfortable at first, research shows this is one of the most effective ways to learn. Instead of your instructor typing code and explaining every character, you are going to read some Ruby code that's already been written. You will likely have some questions about what X or Y is doing, and you'll also likely be able to make some deductions about what other pieces are doing. We will talk through it all after you've had a chance to use your brain and make some connections on your own.

[Look at the code in this repl.it](https://replit.com/@turingschool/oop-intro-ford-escape#main.rb) and think through the guiding questions:

- What is the name of the class?
- How many instances are being made?
- What is the attribute?
- Can you make another instance?

Let’s discuss what you probably found and maybe had questions about.

### Write a New Class

In the previous section, you identified an object in your home and wrote a list of instances and attributes.

In either a repl.it file or Ruby file in Atom, write the Ruby code that would represent that class and instances. Don't forget to print out the instances!

## Access Attributes

With the class you wrote in the previous activity try to print out _just_ one attribute. Does it work?

[You'll need to allow read access with an `attr_reader`](https://www.educative.io/edpresso/what-is-attrreader-in-ruby) inside the class definition, above the `initialize` method.

### Connection to Apps we Use

Now that you’ve seen how this “factory” concept can be used in code, you may be wondering about how this code concept is used within apps we use every day.

We won’t get all the way there in illustrating it today, but, we can look at Instagram for a moment to talk through where we see some use of classes and instances.

<img src="https://try.turing.edu/popup-oop/assets/instagram-oop.png">

## Build Your Own Class

Now that we have an understanding of OOP and have used some Ruby syntax to write classes and create objects from them, we are ready to write a program that generates many instances of a class!

For this final section, you will choose the pace at which you want to work and the level of support you get. Read through the three options below and select the one you feel most comfortable and excited about:

<div class="try-it">
  <h3>Mild 🔥</h3> 
  <p>You will get starter code and some step-by-step directions that walk you through what to do and why you're doing it.</p>
  <p><a href="https://replit.com/@turingschool/oop-mild-starter#main.rb">This is your starter kit.</a></p>
</div>

<div class="try-it">
  <h3>Medium 🔥🔥</h3> 
  <p>You will get some starter code and some direction on what to add to it, but will be pushed to apply all of today's learning without explicit direction at times.</p>
  <p><a href="https://replit.com/@turingschool/oop-medium-starter#main.rb">This is your starter kit.</a></p>
</div>

<div class="try-it">
  <h3>Spicy 🔥🔥🔥</h3> 
  <p>You will not have any starter code for this option. Choose your own topic to make a class and instances of that class. There is no starter kit; create a new file on your own!</p>
</div>

## Storing Many Objects

If you’d like to print out all your sentences with one line of code, one way to do that is by storing them in an array. A couple changes were made from our original code in order to write this solution.

```ruby
class Message
  def initialize(recipient)
    @recipient = recipient
  end

  def create_message
    "To #{@recipient}: Hello!"
  end
end

mom = Message.new("Mom")
bff = Message.new("BFF")

messages = [
  mom.create_message,
  bff.create_message
]

puts messages
```

In OOP, it is common to store instances in a list, or array, like the one above.

## Check For Understanding

[Follow the directions in the README of this repo](https://github.com/turingschool/oop_cfu_am0), and submit your fork in the Google Form! 

<br>
<br>
<br>