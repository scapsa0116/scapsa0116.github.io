---
layout: post
title:      "Metaprogramming"
date:       2020-05-03 15:58:25 -0400
permalink:  metaprogramming
---


### Metaprogramming  makes our code much more flexible. It easily alter the number of attributes in the class and change the hash that we initialize the class. Metaprogramming is the practice of writing code that writes code for us. We can asign attributes (att_accesor) under a variable, that helps us to pull,  values with  specific methods.

#### Ex.


### class People 
### att_acceror :name, :hair_collor, :age

### new_attributes = (name: "Stela", hair_collor: "blond", age: 30)
### stela = People.new(new_attributes)
###           stela.name => "Stela"  or
###           stela.hair_collor => "blond"
