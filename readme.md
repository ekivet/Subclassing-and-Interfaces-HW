---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class?

Member variables may only be accecable to a certain method or instance while static class variables are accesable to the entire class. 

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?

No.  Public member variables do not need getters and setters to change their values.  Private member variables do in order to be modified.

3. What are some benefits of making member variables `private`?

Other people working on the same project can't modify your code.

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?

Class B is considered the super and Class A is considered the sub.  Class B would be the parent class and Class A would be the child.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?

Methods defined in the parent class will be passed down to the child.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?

  The call to getTemperature may be returning a value different than the object double defined in the variable.  Casting would convert the data types.



7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?

Abstract classes must have all methods defined.  Concrete classes just need some.  Specifically whatever methods are unique to that class.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?

You can declare methods in an interface but you cannot implement any method you choose.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.

You cannot create an instance of an abstract class.  You must use a subclass
A final class cannot be extended. An abstract class needs to be extended 

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?

Methods with identical names contained within classes and can override each other in the event that the method instructions for a subclass or parent class varies in every class 
Calling a method on an instance of the child class, the implementation of the method in the child class will be executed.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?

LinkedLists and Arraylists are subclasses of the parent class list.  Polymorphic methods will accept inputs of the parent class and all of its subclasses.  Thus a polymorphic method of type 'List' will also accept 'LinkedLists' and 'ArrayLists'.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
