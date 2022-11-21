<p align="center">
  <img src="EyUSelzWEAUrOpn.jpg" width="600" title="Used">
</p>

# Introduction 

Like most tutorials here we will be talking about the crystal programming language which is a compiled ruby syntax like programming language designed for server side development and automotive systems. This tutorial will go into data types, JSON, ECR, Classes, Modules, Methods, Method Arguments, Arrays, Loaders, Servers and finally building your own router to understand exactly how crystal works as a programming language 

# Overview of crystal

Crystal was a language that is still in the experimental phases which was released back in 2014 with a idea to be more like ruby but compiled. This language is used mainly for server side development and as defined by https://nikolamotor.com/ used as a base for automotive systems. This language is a really odd one but fits a wierd syntax for a compiled language. This language is reallyt for people who also enjoy the ruby syntax with most things such as basic variables, routers, importing and modules and classes being setup differently.

# The basics 

Crystal is an easy language to get around and you can understand such as deep amount about it if you come from ruby. For example below is how you initialize variables.

```crystal
variable1 = "Data" 
```

you can also init variables with `@` symbols which make them instance variables for example.

```crystal
@var : String 
@var2 : String | Int64
```

you can use the `|` to make it a or operator saying that variable can be either String or Integer64. This actually is a decently typed and developed system for variables as most languages do not allow you to do that.

you can also assign multiple variables at once

```crystal
a, b, c = 1, 2, 3
```

pretty simple and readable right?

well now you can also output those statements and variables in different ways using puts like so.

```crystal
a = 1
puts a
puts "#{a}"
```

what about methods? Methods in crystal are a bit wackier to some and have some really useful ways of initializing variables. First off like ruby you can call what function or variable of the method you are assinging a variable to. For example 

```crystal
def function2(data)
  puts data
end

function2(data: "value name")
```

which makes it alot easier to assign certain values using those functions. there are a few ways of defining data as well as you can define the data type of the variable inside of the method like so

```crystal
def (x : String) 
  puts x
end
```

x must be a string for you to work with it. Like definitions and methods we have classes and modules. Starting a class is simple in crystal just use the class keyword followed by the class name and a definition.

```crystal
class Classname 
  def task
    "data" + self
  end
end
```

what this class does is defines a method called task and under that returns or adds a string to the current value so if you wanted to call that function or method you would use.

```crystal
class Classname 
  def task
    "data" + self
  end
end

def Classname.askin
  "Data value two"
end

puts Classname.askin
```

will output 

`Data value two`

The reason this happens is because we are using the class to define a new method not the same method. Also do note that we would need to construct a class named `String` to make this output the way we need to. So for example 

```crystal
class String
  def task
    "data" + self
  end
end

puts "more data".task 
```

this will output 

```
more data data
```

because we called the class name with the data type then proceeded to output a string then adding .task the name of our method under that class. Doing this with other data types is a bit hard as for some reason crystal sees String as a class but every other data type as a structure. So if you switch class String to class Int it will call it a struct and error out. 

this makes code time alot more efficient the further you get into the language and gives you the most basic understanding of how methods can be used. Functions and methods also have return types which you can call in two ways. if you want more than one argument you use `{datatype, datatype}` and if you want to return only one data type you use `:`

for example say we have a method that adds two values and returns the final single value


```crystal
def multiply(x : Int, y : Int) : Int
      return x*y
end
```

will return of typer integer and return the multipled values. So in the after definining a function you can go ahead and mark the return type after the () with : . Now as said before we can use a list of return types using {} which looks a little like this \

```crystal
def afunction : {Int, String}
  return 1, "some string"
end
```

Do you understand how helpful this can actually be? I think this is very neat because of how interesting the type system works with methods and in general. This type of definition will help you in later more advanced code bases with crystal. As you can see the basics of crystal are easy but it does get a bit wackier towards the end but either way still pretty good for a compiled language right?

* Task for this section: Build a basic application that will take the input of a single strign using a class and mash the first and last name together where the first name is static. Do not forget that definitions can not start with a capital letter because it then becomes constant.

<details>
<summary>View Assignment code</summary>
  
  ```crystal
  class String
    def lastname
      "bobert " + self
    end
  end

  puts "Data".lastname
  ```
</details>


