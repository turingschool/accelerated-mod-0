---
layout: page
title: Hashes
---

## Learning Goals

- Use syntax to declare variables that store Hashes in Ruby
- Access data from Ruby Hashes
- Iterate over Hashes with `each`

## Vocabulary

- Hash
- hash rocket
- key
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

## Hashes vs. Arrays

For each example, determine if a Hash or Array would be more appropriate, and explain why. Share your responses in the Mod 0 Slack channel for feedback.
- A store's inventory
- The contents of a dishwasher
- List of all the places you've traveled to
- List of birthdays of all students
- Names of all dogs at doggie daycare
- Virtual address book
- Items of clothing in a dresser

## Hash Syntax Practice

1. For one of the examples in the previous activity that you selected would be best suited for a Hash, declare a variable that stores a Hash with some (possibly fake) data.
1. Declare a variables that stores a Hash that represents [this tweet](https://twitter.com/MechEngSanchez/status/1485947286396014593)

## Exploring Hashes

The following activity is meant to be a CHALLENGE! You will get direct instruction after struggling for a bit with this on your own.

1. Start with the hash: `suitcase = { “socks” => 4, “jeans” => 1 }`
1. Check for how many jackets you have in your suitcase
1. Add 3 shirts to your suitcase
1. Add a key value pair of swimsuit/`true` to your suitcase
1. Take the socks out of your suitcase
1. Check how many shirts (and only shirts) are in your suitcase
1. Call `.keys` and `.values` on your hash - what is returned? Why might this be useful?

<br>
<br>
<br>
<br>

## Accessing a Hash

We use brackets `[]` to access a Hash just like Arrays, only we don’t use indexes, we use _keys_.

Did we put any jackets on our list? Let’s check:
```ruby
suitcase["jackets"]
=> nil
```

We can create a new key/value pair like this:
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
suitcase.keys
=> [1]
```
<br>

**Complete `hashes_1.rb` file [in the CFU repository](https://github.com/turingschool/hashes_cfu_am0) before moving on.**

## Iterating over Hashes

Oftentimes,  we will want to iterate over a Hash to do something with each key/value pair. This works a lot like iterating over an Array, with one small exception. Take a look at the code snippet below and see if you can identify the difference between iterating over a Hash vs over an Array:

```ruby
suitcase.each do |clothing_item, quantity|
	p "I need #{quantity} #{clothing_item}"
end
```

Now, instead of having _one_ block variable to work with, we have two. The first represents the key, and the second represents the value.

**Complete `hashes_2.rb` file [in the CFU repository](https://github.com/turingschool/hashes_cfu_am0).**

<br>
<br>
<br>
<br>