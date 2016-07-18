# Quiz 2 answers:

# 1.
```ruby
a = 1   #set variable "a" to 1
@a = 2  #set instance variable "a" to 2
@@a = 5  #set class variable "a" to 5
user = User.new  #instantiate a User class object named "user"
user.name  #access the instance variable "name" in the instance "user" 
user.name = "Joe"  #set the instance variable "name" in the instance "user" to "Joe"
```

# 2.
A module is like a toolbox for a class. It can contain constants and methods for a class to use.

```ruby
module Skill 
  def hobby
    puts "I love climbing trees!"
  end
end

class Monkey
  include Skill
end

george = Monkey.new
george.hobby
```

# 3.
A class variable belongs to a class (@@var). It can be directly accessed from the class. An instance variable is attached only to the instance of the class (@var) and can only be access through the instance.

```ruby
Class Testing
  attr_accessor :name

  @@number_of_tests = 0  #class variable

  def initialize(name)
    @name = name  #instance variable
  end

  def greeting
    puts "this test is call #{@name}"
  end

  def self.info
    @@number_of_tests
  end
end

test = Testing.new("test 1");
test.name  #to access instance variable

Testing.info  #to access class variable
```

# 4.
A class method is defined by writing *self.method_name* and can be access directily through the class. An instance method is defined with just a *method_name* and can only be access through an instance of the class.

Referring to the code segment in answer 3, *greeting* is an instance method and *self.info* is a class method

```ruby
test = Testing.new("testA")
test.greeting  # => "this test is call testA"

Testing.info # => 0
```

# 5.
```ruby
class User

  def initialize(name, sex, profession)
    @name = name
    @sex = sex
    @profession = profession
  end
end
```

# 6.
A: If *self* is used in a class, inside a method, then self is referring to the instance of the class we created.
B: If *self* is used in a class, outside a method, then self is referring to the class itself. 

# 7.
*attr_accessor* is use to automatically generate a setting and getter method so an instance of the class can directly access an instance variable from outside the class. 

*attr_reader* only generates a getter method and *attr_writer* only generates a setting method, but *attr_accessor* generates both of them.

# 8.
A public method can be accessed from outside the class by the class itself or an instance of the calss. A private method can only be accessed from within the class.

# 9.
Ruby does not support multiple inheritance so a class can only inherit from one class; however, a class can include many modules. 

When we want a class to belong to another class, then we will choose to let the class inherit the other class. When we want the class to possess many different method/actions then using a module is more suitable.

# 10.
If a class includes a module, then its subclass will also be able to access the methods in the module; however, its parent class will not be able to access the methods in the module.

# 11.
Relational Database is a collection of datas that are organized through a set of tables. SQL (Structured Query Language) is a language designed to query through relational database systems. 