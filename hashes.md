---
layout: page
title: Hashes
---

## Learning Goals

- Use Ruby syntax to declare variables that store Hashes
- Access data from Ruby Hashes
- Iterate over Hashes with `each`

## Vocabulary

- Hash
- hash rocket
- key
- key-value pair
- value

## Warm Up

Look at the following array? What is problematic about it? How would you prefer to structure a list of students and such information?

```ruby
students = ["Cristie Soto", "A+", "B", "in progress", true, "Oscar Smith", "A-", "D", "dropped", true]
```
<br><br>

## Hashes

Hashes allow us to structure data in a different way than Arrays. It's not better; it's just different. Like an Array, a Hash is a data structure used for representing a collection of things. But whereas an Array generally represents a list of ordered, indexed values, **a Hash represents a collection of _named_ values**. These names are called **keys**, and each key has a corresponding **value**. In a Hash, we can insert data by assigning it to a name and later retrieving it using the same name.

Some languages call their Hashes _dictionaries_ for this reason – you look up a word (the label) to retrieve its definition (the data or value with which the label was associated).

## Hash Syntax

- A hash is enclosed in curly braces `{ }`, key/value pairs are separated by commas, and keys and values are separated by either a **hash rocket (`=>`)** or a colon.
- Each key in a hash must be unique
  - If you attempt to have duplicate keys when you first create a hash, you will get a warning: `key :key_name is duplicated and overwritten on line X error`
  - If you try to add a new key/value pair using a key that already exists, that new key/value pair will overwrite the previous one - _dangerous_.
- Keys and values can be any type of object:
```ruby  
student1 = {
    "name" => "Christie Soto",
    "grades" => ["A+", "B", "in progress"],
    "active_student" => true
}
```
- Values can be accessed with bracket notation:
  - `student1["name"]` returns `"Christie Soto"`

<div class="try-it">
  <h3>Hash or Array?</h3> 
  <p>For each example, determine if a Hash or Array would be more appropriate, and explain why. Share your responses in the Slack small group channel for feedback and discussions.</p>
  <ul>
    <li>A store's inventory</li>
    <li>The contents of a dishwasher</li>
    <li>List of all the places you've traveled to</li>
    <li>List of birthdays of all students</li>
    <li>Names of all dogs at doggie daycare</li>
    <li>Virtual address book</li>
    <li>Items of clothing in a dresser</li>
  </ul>
</div>

<div class="try-it">
  <h3>Hash Syntax Practice</h3> 
  <p>Complete the following work in an <code>irb</code> session or a new Ruby file, working in Atom:</p>
  <ol>
    <li>For one of the examples in the previous activity that you selected would be best suited for a Hash, declare a variable that stores a Hash with some (possibly fake) data.</li>
    <li>Declare a variable that stores a Hash that represents <a href="https://twitter.com/MechEngSanchez/status/1485947286396014593" target="blank">this tweet</a></li>
  </ol>
  <p>Take a screenshot or save in this work in a file and be ready to share it in Stand Up tomorrow!</p>
</div>

## Accessing a Hash

We use brackets `[]` to access a Hash just like Arrays, only we don’t use index positiona, we instead use _keys_.

The examples below explore the `suitcase` Hash:

```ruby
suitcase = { 
  "socks" => 4, 
  "jeans" => 1
}
```

Did we put any jackets on our list? Let’s check:
```ruby
suitcase["jackets"]
=> nil
```

We can create a new key-value pair:
```ruby
suitcase["shirts"] = 3
suitcase["swimsuit"] = true
```

We can remove the socks:
```ruby
suitcase["socks"] = nil
```

or

```ruby
suitcase.delete("socks")
```

Check on the shirts:
```ruby
suitcase["shirts"]
=> 3
```

Let's check what keys are in our Hash:
```ruby
suitcase.keys
=> ["jeans"]
```

Let's check what values are in our Hash:
```ruby
suitcase.values
=> [1]
```
<br>

<div class="try-it">
  <h3>Hash Syntax and Access Practice</h3> 
  <p>Use the following <code>foods</code> variable to complete each prompt:</p>
  <pre>
  zoo = {
    "giraffes" => 3,
    "zebras" => 12,
    "hippos" => 2
  }
  </pre>
  <ol>
    <li>Print all of the keys of the zoo Hash</li>
    <li>Print all of the values of the zoo Hash</li>
    <li>Print the value of the first animal of the zoo</li>
    <li>Add an animal to the zoo</li>
    <li>Check how many monkeys are in the zoo</li>
    <li>Add another animal to the zoo</li>
    <li>Print all of the keys of the zoo Hash</li>
  </ol>
</div>

<div class="try-it">
  <h3>Hash Syntax Refactor</h3> 
  <p><a href="https://gist.github.com/ameseee/af01754c4c5d433657b913e44e35d9c6" target="blank">Refactor the code in this Gist</a> to improve the style and syntax (think: readability) of the Hashes.</p>
</div>
<br>

## Iterating over Hashes

Oftentimes,  we will want to iterate over a Hash to do something with each key/value pair. This works a lot like iterating over an Array, with one small exception. Take a look at the code snippet below and see if you can identify the difference between iterating over a Hash vs over an Array:

```ruby
suitcase.each do |clothing_item, quantity|
	p "I need #{quantity} #{clothing_item}"
end
```

Now, instead of having _one_ block variable to work with, we have two. The first represents the key, and the second represents the value.

## Check For Understanding

Complete the work [in the CFU repository](https://github.com/turingschool/hashes_cfu_am0) and submit your work using the submission form. Read the README carefully; it calls for submission of the Refactor Gist as well!

<br>
<br>
<br>
<br>