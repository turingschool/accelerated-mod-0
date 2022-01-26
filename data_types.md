---
layout: page
title: Data Types
---

## Learning Goals

- Identify and use 3 basic Data Types
- Assign and reassign variables in Ruby
- Comfortably use IRB within the Terminal

## Vocabulary

- assignment operator
- Boolean
- Data Type
- Float
- Integer
- IRB (interactive Ruby)
- String
- variable

## Where To Run Code

By the end of this session, you'll be able to use the your Terminal, specicially a tool called `irb`, to run and check your code. This is a great tool for a beginner, as well as a seasoned software developer, to have. `irb` will allow you to explore and learn Ruby and test out code you've written in a low stakes environment. It is quick and easy to open up the terminal and run your code immediately.

### `irb`: Tips & Tricks

- Open and close the Terminal quickly with keyboard shortcut `cmd + space` to open Spotlight. Then start typing "terminal" and it should auto-fill. Press `return`. _Note: there are other ways to open your Terminal but keyboard shortcuts are most efficient and the norm in the industry_
- Regardless of your working directory, you can type `irb` then press `return` to open up an what is referred to as an "irb session". A prompt that looks something like `irb(main):001:0>` will appear; you'll eventually type code to the right of that
- The font size of your terminal can be increased or decreased with shortcuts `cmd + +` or `cmd + -`
- To exit the irb session, type `exit` in all lowercase, then press `return`

<div class="try-it">
  <h3>Practice: <code>irb</code></h3> 
  <ul>
    <li>Open the Terminal using Spotlight.</li>
    <li>Open an irb session</li>
    <li>Increase the size of your font</li>
    <li>Exit the irb session</li>
  </ul>
</div>

## Data Types

In this lesson, we will use 4 of Ruby's Data Types:
- **String** - Any series of characters (alpha, numeric, or symbol) between quotation marks
- **Integer** - Any whole positive and negative number, including 0
- **Float** - Any positive and negative number that involves a decimal
- **Boolean** - `true` or `false`

To connect to how these data types are used in an application we all have some experience with, consider the steps you took to enroll at Turing in the Populi application:
- **String** - You provided your email address and it was stored as a string, for example: `"helloworld@gmail.com"`
- **Integer** - You provided your date of birth and the program calcalated your age, for example: `37`
- **Float** - You paid your deposit and that amount was stored as `1200.00`
- **Boolean** - Once you paid your deposit, the "paid deposit" field said `true`

## Variables

Pieces of data in the various types we've discussed so far are valid Ruby code just as they are. We can demonstrate that by typing `"helloworld@gmail.com"` or `37` or `false` into irb. We know they are valid because we don't get an error. If `helloworld@gmail.com` is typed in, we _will_ get an error, and possibly a helpful suggestion! 

However, if we ever want to reference that email address ever again in our code, the only way would be to read that part of the screen and manually type it out again - and that's not going to make for a very efficient application.

**Variables** are what allow us to store data in a Ruby program. We can think of them as storage containers that hold items we care about and want to keep track of. The label on top of that container is what we can compare to a variable _name_. Variables can store any of the Data Types we've learned today as well as others that you'll learn about in upcoming lessons.

### Variable Syntax

In Ruby, we declare variables by typing the name of the variable, the **assignment operator**, then the value being stored.

```ruby
email = "helloworld@gmail.com"
starting_age = 37
amount_paid = 1200.00
deposit_paid = true
```

>To describe the first line of code in the previous example, one might say "This line of code declares a variable named `email` and assigns it to the String of `helloworld@gmail.com`".

If our Ruby program has data stored in variables, we are able to reference those variables at any time to access the data. This can be demonstrated in irb.

### Best Practices for Naming Variables

Naming can be hard, but is important to be thoughtful about and follow conventions of the language you are working with so that your code is easily accessible and readable for those you are collaborating with. A few key points:
- All Ruby variables should use `snake_case` - all characters should be lower cased; in multi-word variables, words should be separated with an underscore
- Variable names should descirbe the type of data they hold without being overly verbose or specific (examples: `name`, `email`, etc. non-examples: `x`, `ftga23`, `name_of_incoming_mod_1_be_student`)

### Reassigning Variables

We often need to write code that changes the data stored in a variable. Consider this Populi example:
- When a student first creates a profile, the `deposit_paid` variable is automatically assigned to `false`
- Once the student pays their deposit, some code is triggered to change that value to `true`

To do that, we use the exact same syntax that we used to make the original assignment. We can run the code that follows, or code like it, in irb to demonstrate that the value has changed.

```ruby
deposit_paid = false
deposit_paid # false

deposit_paid = true
deposit_paid # true
```

<div class="try-it">
  <h3>Variables Practice</h3>
  <ul>
    <li>Open an irb session</li>
    <li>Declare 4 variables; a String, Integer, Float, and Boolean</li>
    <li>Call each variable to confirm it was stored correctly</li>
    <li>Reassign each variable to a new value, then call it again to confirm it does indeed store the new value</li>
    <li>Exit the irb session</li>
  </ul>
</div>

## Check For Understanding

_Complete this CFU after you've done the live GitHub lesson._

Use everything you’ve learned with Git, GitHub, Data Types and variables, complete this challenge:

1. Create a new directory called `variable_practice`
1. Inside that directory, create a file called `variables.rb`
1. Initialize `git` inside of the directory
1. Commit your work (Think about what message should you use here)
1. Go to GitHub and create a repo with the same name - `variable_practice`
1. Push your local directory to GitHub by following the instructions
1. In your `variables.rb` file, add a few variables that are assigned to Strings
1. Commit your work
1. In your `variables.rb` file, add a few variables that are assigned to Integers
1. Commit your work
1. In your `variables.rb` file, add a few variables that are assigned to Floats
1. Commit your work
1. In your `variables.rb` file, add a few variables that are assigned to Booleans
1. Commit your work
1. In your `variables.rb` file, leave the original String variables as declared, but add some code to _reassign_ them to different values
1. Commit your work
1. Annotate at least 3 of the lines of code in `variables.rb`
1. Commit your work
1. Push your changes to GitHub

<br><br>