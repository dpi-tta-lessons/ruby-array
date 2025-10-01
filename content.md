# Ruby Array

Work with lists of data in Ruby using the Array class.

## Goal

By the end of this lesson, you'll be able to *create*, *add*, *retrieve*, and *use* data from arrays in Ruby.

<div class="alert alert-info">
  <ul>
    <li><a href="https://www.youtube.com/watch?v=qlKQzgGGsi80">Video (with Margo)</a></li>
    <li><a href="https://youtu.be/ht18qm_JOJM">Video (with Amanda)</a></li>
  </ul>
</div>

## What is an Array?

An array is a list. Think of it like a row of boxes, each holding an item. You can add more boxes, take things out, and check what's inside.

In Ruby, arrays can hold any type of object—numbers, strings, even other arrays.

<aside class="tip">
  Arrays are one of the most common data structures in programming, you'll use them almost everywhere.
</aside>

## Create an Empty Array

We can create a new empty array with `Array.new`:

```ruby
foods = Array.new
pp foods.class
pp foods
```
{: .repl }

<aside class="tip">
  Ruby represents an Array with square brackets, <code>[]</code>.
</aside>

## Add Items with `push`

Let's put some foods into our array using [push](https://docs.ruby-lang.org/en/master/Array.html#method-i-push):

```ruby
foods = Array.new

foods.push("Pizza")
foods.push("Sushi")
pp foods 
```
{: .repl }

<aside class="tip">
  Try adding more food items to the <code>foods</code> array using the <code>push</code> method.
</aside>

## Shortcut with Array Literals

Instead of using `Array.new` + `push`, we can write arrays directly with square brackets. We can type an array "literal" directly into the code:

```ruby
foods = ["Pizza", "Sushi", "Pineapple"]
pp foods
```
{: .repl }

### Get Items with `at` or `[]`

We can grab items by their position (index). Ruby starts counting at 0.

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods.at(0)   # First item
pp foods.at(2)   # Third item
pp foods.at(-1)  # Last item
```
{: .repl }

Syntax Sugar: use square brackets `[]` instead of `at`.

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods[0]   # "Pizza"
pp foods[2]   # "Pineapple"
pp foods[-2]  # "Curry"
```
{: .repl }

## `first` and `last`

Ruby has shortcuts to grab the first or last item:

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods.first
pp foods.last
```
{: .repl }

## `count`

How many items are in an array?

```ruby
a = [8, 3, 1, 19, 23, 3]

pp a.count

pp a.count(3)
```
{: .repl }

## Random Items with `sample`

Pick a random element from an array. Each time you run it, you may get a different result.

```ruby
an_array = [8, 3, 1, 19, 23, 3]

pp an_array.sample
```
{: .repl }

## `min`, `max`, and `sum`

Ruby can do simple math on arrays of numbers:

```ruby
a = [8, 3, 1, 19, 23, 3]

pp a.min
pp a.max
pp a.sum
```
{: .repl }

## Quiz

```ruby
foods = ["Pizza", "Sushi", "Curry"]
pp foods.at(1)
```

- What does this code print?
- "Pizza"
  - Not correct. Remember, arrays start at index 0.
- "Sushi"
  - Correct! Index 1 is the second item.
- "Curry"
  - Not correct. That's index 2.
{: .choose_best #array_index title="Array Indexing" answer="2"}

## Project: Array

In this project, you will write Ruby programs that leverage these Array methods. This project includes automated tests, so click this link to get started <https://github.com/dpi-tta-projects/ruby-array/fork>, fork the repository and create a codespace.

<aside class="warning">
  In order to get credit for completing this project you'll need to open the assignment link from canvas to generate an access token.
</aside>

## References

- [Ruby Docs: Array](https://docs.ruby-lang.org/en/master/Array.html)
