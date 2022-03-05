---
layout: lesson
title: Conditionals
---

## Learning Goals

- Use comparison and logical operators
- Write if/elsif/else statements for conditional logic

## Vocabulary

- <span class="vocab">comparison operators</span>
- <span class="vocab">logical operators</span>
- <span class="vocab">conditionals</span>
- <span class="vocab">if statements</span>

## Comparison Operators

_This will connect to Booleans, which you learned about in the Data Types lesson._

Conditional statements, or <span class="vocab">conditionals</span>, are Ruby statements that evaluate to `true` or `false`. The most common operators used for conditions are <span class="vocab">comparison operators</span>:

- `==` (equal)
- `!=` (not equal)
- `>` (greater than)
- `>=` (greater than or equal to)
- `<` (less than)
- `<=` (less than or equal to)

<div class="s-card s-border-yellow-500">
  <h4>Equality vs. Assignment</h4>
  <p>The number one mistake people encounter when writing conditional statements is the difference between <code>=</code> and <code>==</code>.</p>
  <ul>
    <li><code>=</code> is an assignment. It means "take the value on the right side and store it into whatever is on the left side" – it’s telling, not asking.</li>
    <li><code>==</code> is a question. It means "is the value on the right the exact same as the value on the left?" – it’s asking, not telling.</li>
  </ul>
</div>

[Read more about comparison operators.](http://ruby-for-beginners.rubymonstas.org/operators/comparison.html)

<div class="s-card">
  <h3>Comparisons</h3>
  <p>Complete the following work in an <code>irb</code> session:</p>
  <ul>
    <li>Check if 3 is less than or equal to 6.</li>
    <li>Check if "T" is equal to "t".</li>
    <li>Check if "P" is equal to " P".</li>
    <li>Check if 10 is not equal to 10.</li>
    <li>Declare a variable that store your name in a String.</li>
    <li>Check if the length of your name is greater than or equal to 10 (not sure how to do that programmatically? Google!)</li>
  </ul>
</div>

## Logical Operators

There are 3 <span class="vocab">logical operators</span> in Ruby; we will learn 2 today:
- `&&` or `and`
- `||` or `or`

### `&&` or `and`
This logical operator will check two values, and both **must** be true in order for it to return `true`. Examples follow:

```ruby
age = 34
time = 2.05

age < 40 && time < 3.0
# true (both meet requirement)

age < 30 && time < 3.0
# false (age is not less than 30)

age < 40 && time < 2.0
# false (time is not less than 2.0)

age < 30 && time < 2.0
# false (neither meet requirement)
```

### `||` or `or`
This logical operator will check two values, and _one_ or _both_ must be true in order for it to return true. Examples follow:

```ruby
age = 34
time = 2.05

age < 40 || time < 3.0
# true (both meet requirement)

age < 30 || time < 3.0
# true (time meets requirement)

age < 40 || time < 2.0
# true (age meets requirement)

age < 30 || time < 2.0
# false (neither meet requirement)
```

<div class="s-card">
  <h3>Logical Operators</h3>
  <p>Complete the following work in an <code>irb</code> session:</p>
  <ul>
    <li>Declare two variables - one that stores your age and another person's age.</li>
    <li>Check if both ages are under 100.</li>
    <li>Check if at least one age is under 78.</li>
    <li>Check if your age is over 18 and the other age is under 60.</li>
    <li>Check if your age is over 21 or if the other age is over 25.</li>
    <li>Check if your age is under 20 or if the other age is over 40.</li>
  </ul>
</div>

## If Statements

<span class="vocab"><code>If statements</code></span> are the most common form of conditionals. The logic of an <code>if statement</code> in Ruby follows the same logic in other programming languages.

### `if`
All of our conditional branches will begin with an `if`. The code following the `if` will run if the condition is true.

```ruby
if condition
  # code to execute if condition evaluates to true
end
```

<div class="s-card">
  <h3><code>if</code> statements</h3>
  <p>In an <code>irb</code> session, write code that defines an <code>age</code> variable and assign it to an Integer. Then, write code that will print out the String "Welcome to the Website" only if the user is 21 or older.</p>
</div>
<br>

### `elsif`
Use an `elsif` to create more branches.

```ruby
if condition1
  # code to execute if above condition1 evaluates to true
elsif condition2
  # code to execute if above condition2 evaluates to true
elsif condition3
  # code to execute if above condition3 evaluates to true
end
```

<div class="s-card">
  <h3><code>elsif</code> statements</h3>
  <p>In an <code>irb</code> session, write code that defines an <code>age</code> variable and assign it to an Integer. Then, write code that will print out the String "Welcome to the Website" only if the user is 21 or older. If the user is under the age of 2, print out "How are you even on this device?".</p>
</div>
<br>

### `else`
Code inside an `else` will run when none of the previous conditions are true.

```ruby
if condition1
  # code to execute if above condition1 evaluates to true
elsif condition2
  # code to execute if above condition2 evaluates to true
elsif condition3
  # code to execute if above condition3 evaluates to true
else
  # code to execute if all previous conditions evaluate to false
end
```
<div class="s-card">
  <h3><code>else</code> statements</h3>
  <p>In an <code>irb</code> session, you'll build on the previous work you've done with the <code>age</code> variable. Write code that will print out the String "Welcome to the Website" only if the user is 21 or older. If the user is under the age of 2, print out "How are you even on this device?". If the user is any other age, print out "You aren't quite old enough to visit, sorry!".</p>
</div>
<br>

Notice that each of the previous examples have **one** `end` keyword. That is paired with the opening `if` keyword, and is required. [What happens if you forget the `end` keyword?](https://teamtreehouse.com/community/syntax-error-unexpected-endofinput-expecting-keywordend)

>_Optional:_ Read the [Conditionals section](http://tutorials.jumpstartlab.com/projects/ruby_in_100_minutes.html#9.-conditionals) from Ruby in 100 Minutes for a different explanation.

<br>
<div class="s-card">
  <h3>More Practice</h3>
  <p>Complete the following work in an <code>irb</code> session:</p>
  <ul>
    <li>Declare a variable that stores your name in a String.</li>
    <li>Write an if/else statement - if your name is "Oscar", puts "Hello, Oscar!". If not, puts "Hello, Stranger!".</li>
    <li>Challenge: Use string interpolation to interpolate any non-Oscar name in after the word "Stranger".</li>
  </ul>
</div>

## Check For Understanding

[Follow the directions in the README of this GitHub repository](https://github.com/ameseee/conditionals-cfu-am0), and submit your fork in the submission form. Upload the video (requirements outlined in the GitHub repo) to your Slack small group channel.
<br><br><br>
