# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Intro Ruby Training Solutions

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

## Conditionals & Loops

```rb
# 1. Print (`puts`) "Ruby is awesome!" 50 times.
# Implement this 3 different ways, using:

  # `while`
  i = 0
  while i < 50
    puts "Ruby is awesome!"
    i += 1
  end

  # `for`
  for i in (1..50)
    puts "Ruby is awesome!"
  end

  # `times`
  50.times do
    puts "Ruby is awesome!"
  end

# 2. Save any string to a variable, then create an empty hash called
# count (`count = {}`). Loop through the string, and count occurrences
# of each letter. Store the counts in your hash like this example:
  # For the string `apple`, your `count` hash would look like this:
  # `{a: 1, p: 2, l: 1, e: 1}`.
  str = "banana"
  count = {}
  i = 0
  while i < str.length
    if count[str[i]]
      count[str[i]] += 1
    else
      count[str[i]] = 1
    end
    i += 1
  end

# 3. Write a program that gets user input from the terminal and `puts` it until
# the input is the word `"quit"` or `"q"`.
input = nil
while input != "quit" && input != "q"
  puts input if input
  puts "Enter input here:"
  input = gets.chomp
end

```

## Stretch Challenges

```rb
# Iterators: Each

# 1. Define an array of 4 phrases: `"Hello, world"`, `"OMG"`, `"Ruby"`,
# and `"Pair Programming"`. Use `.each` to iterate over the array and
# `puts` each phrase.
phrases = ["Hello, world", "OMG", "Ruby", "Pair Programming"]
phrases.each do |phrase|
  puts phrase
end

# 2. Iterate over your array of phrases again, but this time, only
# `puts` the phrase if its length 5 letters or longer. Otherwise,
# print a message that the phrase is too short, and include the phrase's
# index in the message (Hint: Look up `.each_with_index`).
phrases.each_with_index do |phrase, index|
  if phrase.length >=5
    puts phrase
  else
    puts "Phrase at index #{index} is too short."
  end
end
```

```ruby
# Iterators: Map

# 1. Write a program that maps an array of numbers to double each number.
arr = [1, 2, 3]
mapped_arr = arr.map {|num| num * 2}

# 2. Write a program that maps an array of words to the reverse of each
# word. (Hint: Look up `.reverse`)
words = ["San Francisco", "General Assembly", "web development"]
mapped_words = words.map {|word| word.reverse}
```

```rb
# Create a simple temperature convertor.
puts "Type '1' to convert from Celsius to Fahrenheit or '2' to convert from Fahrenheit to Celsius"
response = gets.chomp

if response == "1"
  puts "Enter Celsius temperature:"
  temp = (gets.chomp).to_i
  f_temp = (temp * 9/5) + 32
  puts "#{temp} degrees Celsius is equal to #{f_temp} degrees Fahrenheit"

elsif response == "2"
  puts "Enter Fahrenheit temperature:"
  temp = (gets.chomp).to_i
  c_temp = (temp - 32) * (5/9)
  puts "#{temp} degrees Fahrenheit is equal to #{c_temp} degrees Celsius"
end
```

```ruby
# Create a simple calculator that first asks the user what method
# they would like to use (addition, subtraction, multiplication, or
# division), then asks the user for two numbers, printing the result
# of the method with the two numbers.
puts "What calculation would you like to do? (add, sub, mult, div)"
response = gets.chomp

puts "What is the first number?"
num1 = (gets.chomp).to_f

puts "What is the second number?"
num2 = (gets.chomp).to_f

if response == "add"
  result = num1 + num2

elsif response == "sub"
  result = num1 - num2

elsif response == "mult"
  result = num1 * num2

elsif response == "div"
  result = num1 / num2
end

puts "The result is #{result}"

# alternate solution (using case)
puts "What calculation would you like to do? (add, sub, mult, div)"
response = gets.chomp

puts "What is the first number?"
num1 = (gets.chomp).to_f

puts "What is the second number?"
num2 = (gets.chomp).to_f

case response
  when "add" then result = num1 + num2
  when "sub" then result = num1 - num2
  when "mult" then result = num1 * num2
  when "div" then result = num1 / num2
end

puts "The result is #{result}"
```

```ruby
# Write a program that prints the "bottles of beer on the wall" song.
verses = gets.chomp.to_i
while verses > 0
  puts "#{verses} bottles of beer on the wall,"
  puts "#{verses} bottles of beer!"
  puts "Take one down and pass it around,"
  verses -= 1
  if verses == 1
    puts "#{verses} bottle of beer on the wall!"
  elsif verses == 0
    puts "No more bottles of beer on the wall."
  else
    puts "#{verses} bottles of beer on the wall!"
  end
  puts "----------"
end
```
