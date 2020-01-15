---
layout: post
title:      "'#RUBY key concepts of CLASSES and INSTANCES'"
date:       2020-01-15 00:24:22 -0500
permalink:  ruby_key_concepts_of_classes_and_instances
---


### *Classes  produces individual objects!  Each of which contains all the information and behaviors of an individual object.
### Ruby classes both contains, the instructions for creating new objects, and has the ability to create those objects. We define a class with the "class" keyword, and is ending with the "end " keyword. A class is compared with the blueprint that defines how to build an object, and very important to subline that the class is building the actual behavior of an object.
### Every method in the class should conein the "def" keyword and should be close with an "end".
## 
####  
####  1. ex
####  class Family 
####  
####     def talk
####   puts "Hello"
####      end 
####  
####  end  
* 
### Instantiate of a class means bringing a new object to life, instances refer to the individual objects produced from the class. We can build multiple instances of only one class, that means we can bring more objects to life ,that belongs to one class. Ruby's  return value is called Ruby Object Notation, and its the way that we can see that instance belongs to a particular class. Instance of a class is build with the key word of the class.new and it doesnt have an ending define. A new instance will behave along with the called  block from the class. 
###  *

####  
####  2. ex 
####   member = Family.new 
####   member.talk  #will output "Hello"
####  
####   
####   member - instance 
####   Family - class 
####  *
