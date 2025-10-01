# Ruby Array

Store, organize, and manipulate lists of data.

## Goal

By the end of this lesson you'll be able to create and manage lists of data using the `Array` class.

<div class="alert alert-info">
  <ul>
    <li><a href="https://www.youtube.com/watch?v=qlKQzgGGsi80">Video (with Margo)</a></li>
    <li><a href="https://youtu.be/ht18qm_JOJM">Video (with Amanda)</a></li>
  </ul>
</div>

## What is an Array?

An array is a list of items. Think of an array as a container for other objects that can hold however many objects we want. The [Array class](https://docs.ruby-lang.org/en/master/Array.html) provides methods that help manage lists of items.

## Creating Arrays

You can create an array using an initializer `new`"

```ruby
foods = Array.new
pp foods.class
pp foods
```
{: .repl }

## Array Methods

### `push`

Ruby represents an Array with square brackets, `[]`. How can we add elements to an empty array? We can use the `push` method.

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

## Array Literals

There's a shortcut to creating Arrays. We don't have to instantiate the Array class every time with Array.new and build it from scratch with the .push method. We can type an array "literal" directly into the code:

```ruby
foods = ["Pizza", "Sushi", "Pineapple"]
pp foods
```
{: .repl }

What will the output of the above snippet be?

### `at`

`push` lets us add elements to our array list. The next thing we need to be able to do is to retrieve an element from the list we've created. We can use .at to do this.

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods.at(-2)
```
{: .repl }

What will the output of the above snippet be?
 
The `at` method will take an `Integer` argument which is interpreted as the position or index in the `Array` of the element that you want to retrieve.

### `at` shorthand, `[]`

You can substitute the `at` method with square brackets `[]`

What will the output of the above snippet be?

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods.[](2)
```
{: .repl }

What will the output of the snippet be?

Syntactic sugar:

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods[2]
```
{: .repl }


## `first` and `last`

What will the output of the snippet be?

```ruby
foods = ["Pizza", "Sushi", "Pineapple", "Curry", "Sandwich"]

pp foods.first
pp foods.last
```
{: .repl }

## `count`

```ruby
a = [8, 3, 1, 19, 23, 3]

pp a.count

pp a.count(3)
```
{: .repl }

What will the output of the above code snippet be?

## `sample`

What will the output of the code snippet be?

```ruby
an_array = [8, 3, 1, 19, 23, 3]

pp an_array.sample
```
{: .repl }

## `min`, `max`, and `sum`

What will the output of the code snippet be?

```ruby
a = [8, 3, 1, 19, 23, 3]

pp a.min
pp a.max
pp a.sum
```
{: .repl }

## Project: I/O

In this project, you will write Ruby programs that leverage these Array methods. This project includes automated tests, so click this link to get started <https://github.com/dpi-tta-projects/ruby-array/fork>, fork the repository and create a codespace.

<aside class="warning">
  In order to get credit for completing this project you'll need to open the assignment link from canvas to generate an access token.
</aside>

## References

- [Ruby Docs: Array](https://docs.ruby-lang.org/en/master/Array.html)
