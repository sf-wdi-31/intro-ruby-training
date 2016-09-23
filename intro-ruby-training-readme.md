# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Intro Ruby Training

## Data Types & Variables

```rb
# 1. Store your `first_name` in a variable and your `last_name`
# in another variable.
first_name = "Bob"
last_name = "Smith"

# 2. Concatenate your `first_name` and `last_name` variables,
# and store the output in a new variable called `full_name`.
full_name = "#{first_name} #{last_name}"

# 3. Use `.split` to turn your `full_name` variable into an array.
full_name.split
```

### Conditionals & Loops

1. Print (`puts`) "Ruby is awesome!" 50 times. Implement this 3 different ways, using:
  * <a href="http://www.tutorialspoint.com/ruby/ruby_loops.htm" >`while`</a>
  * <a href="http://www.tutorialspoint.com/ruby/ruby_loops.htm" >`for`</a>
  * <a href="http://ruby-doc.org/core-2.0.0/Integer.html#method-i-times" >`.times`</a>

2. Save any string to a variable, then create an empty hash called count (`count = {}`). Loop through the string, and count occurrences of each letter. Store the counts in your hash like this example:
  * For the string `apple`, your `count` hash would look like this: `{a: 1, p: 2, l: 1, e: 1}`.

3. Write a program that gets user input from the terminal and `puts` it until the input is the word `"quit"` or `"q"`.
  * **Hint:** Use `gets.chomp` instead of `gets` to remove trailing `\n`.


## Stretch Challenges

### Iterator Methods

1. Define an array of 4 phrases: `"Hello, world"`, `"OMG"`, `"Ruby"`, and `"Pair Programming"`. Use `.each` to iterate over the array and `puts` each phrase.

2. Iterate over your array of phrases again, but this time, only `puts` the phrase if its length is 5 letters or longer. Otherwise, print a message that the phrase is too short, and include the phrase's index in the message (**Hint:** Look up `.each_with_index`).

1. Write a program that <a href="http://ruby-doc.org/core-2.2.0/Array.html#method-i-map" >maps</a> an array of numbers to double each number.

2. Write a program that maps an array of words to the reverse of each word. (**Hint:** Look up `.reverse`)


### Temperature Converter

Create a simple temperature convertor. It should function like the example below:

  ```
  Type '1' to convert from Celsius to Fahrenheit or '2' to convert from Fahrenheit to Celsius
  1
  Enter Celsius temperature:
  24
  24 degrees Celsius is equal to 75.2 degrees Fahrenheit
  ```

### Calculator

Create a simple calculator that first asks the user what method they would like to use (addition, subtraction, multiplication, or division), then asks the user for two numbers, printing the result of the method with the two numbers. Here is a sample prompt:

  ```
  What calculation would you like to do? (add, sub, mult, div)
  add
  What is the first number?
  3
  What is the second number?
  6
  The result is 9
  ```

### Beer song

Write a program that prints the "bottles of beer on the wall" song:

  ```
  5 bottles of beer on the wall,
  5 bottles of beer!
  Take one down and pass it around,
  4 bottles of beer on the wall!
  ...
  ```

  * Use `gets.chomp` to ask the user how many verses they want to hear.
  * Make sure your song prints "1 **bottle** of beer".
  * When the song gets to "0 bottles of beer on the wall", it should print "No more bottles of beer on the wall" instead.
