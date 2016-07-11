# Quiz 1 answer:


# 1. 
The difference between a Fixnum and a Float is that a Float has decimal places.


# 2.
```ruby
puts str1 + str2
```
This method prints out the two strings by concatenating them together
```ruby
puts "#{str1}#{str2}"
```
This method uses string interpolation which directly inserts the value of the variable into the corresponding token. 


# 3. 
An array contains values that are accessible with spefic indexes. Indexes are integers starting from 0 and onwards. 
```ruby
arr = [0, 1, "a", ["hi", "there"]]
```
A hash has both a key and a value. Each value is accessible with it's corresponding key.
```ruby
test = {
  :name => "Deb",
  :age => 21,
  :food => "fries",
}
```


# 4.
```ruby
[1, "a string", 3.14, [1,2,3,4]].select { |x|  x if x.class != String }
```

# 5.
```ruby
(1..100).each { |x| puts x + 2}
```

# 6.
```ruby
[1, 2, 3, 3].uniq
# => [1, 2, 3]
```
This returns a new array by removing any duplicated values. 
```ruby 
[1, 2, 3, 3].uniq!
# => [1, 2, 3]
```
This returns the changed array after removing any duplicates or returns nil if no duplicates are found.

# 7. 
method 1
```ruby
arr = [5,6,7,8,9]
arr.shuffle!
```
method 2
```ruby
rand(5..9)
```


# 8.
```ruby
((1 > 3)&&(true == true))||(!!!false)
```
This will return true. 
(false && true) || (true) = false || true = true


# 9. 
binding.pry is used when debugging. It acts as a breakpoint and halts the program where the "binding.pry" statement is placed.


# 10.
```ruby
var = 5
return var >= 5 ? "var is greater than or equal to 5" : "var is less than 5"
```


# 11.
```ruby
#method one
arr1 = {
  :name => "Bob",
  :age => 30,
  :pet => "cat"
}

#method two
arr2 = {
  name: "Bob",
  age: 30,
  pet: "cat"
}
```