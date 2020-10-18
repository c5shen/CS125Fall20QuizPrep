# Quiz Preparation for Week 8

### Concepts
  * [Abstract](#abstract)
  * [Interface](#interface)
  * [Anonymous Class](#anonymous-class)
  * [Lambda Expression](#lambda-expression)

### EMP Session Links
1. [EMP 10-15](https://cs199emp.netlify.app/dist/2020-10-15.html): Topics including reference/abstract/interface

### Quick Concept Overview & Practice
#### Abstract
  1. Can be applied to both classes and methods, e.g.:
  ```java
    public abstract class Shape {
      // remember, abstract method doesn't have a body
      public abstract int sides();
    }
  ```
  2. An _abstract class_ may or may not contain _abstract methods_, but if you want to have _abstract method(s)_, the class needs to be abstract. The following is wrong:
  ```java
    public class Shape {
      public abstract int sides();
    }
  ```
  3. An _abstract class_ **cannot** be instantiated (you can't create an instance for an abstract class).
  4. An _abstract class_ **can** be extended (you can have another class extends an abstract class and calls its methods). Children classes need to implement the abstract methods, else they also need to be abstract.
##### Practice 1
Design an abstract class _Cashier_ with two methods: one is an _instance method_ named **receipt** that takes in an amount of money (double), and returns a String as "Total is xxx dollars"; the other is an _abstract instance method_ named **getCategory** which you are too lazy to implement yet.
<details>
<summary>Spoiler!</summary>

```java
  public abstract class Cashier {
    public String receipt(double money) {
      return "Total is " + Double.toString(money) + " dollars";
    }
  }
```
</details>

---

#### Interface
  1. A java class can only extends from one parent, but it can implement multiple interfaces. It means **it supports the functionalities declared in the interfaces**. E.g.:
  ```java
    interface A {
      int funcA();
    }
    interface B {
      int funcB();
    }
    public class Parent { }
    public class Alphabet extends Parent implements A, B {
      public int funcA() {
        return 1;
      }
      public int funcB() {
        return 2;
      }
    }
  ```
  2. Interface works similarly with polymorphism/inheritance. You can have a variable of an interface type and it can refer to the classes that implements the interface. E.g.:
  ```java
    // given the codes in (1)
    A a = new Alphabet();
    // this code returns 1
    int some = a.funcA();
    // this code gives error because interface A does not have funcB() supported
    int other = a.funcB();
  ```
  3. **Comparable** is a built-in java interface that allows you to implement the _compareTo()_ method for instance comparison.
  4. **Iterator, Iterable** are two other built-in java interfaces that allow you to implement methods for enhanced for-loop (iterating items).
##### Practice 2

---

#### Anonymous Class
  1. An _anonymous class_ does not have a name, must extend a class or implement an interface, is created immediately, and cannot provide a constructor. Syntax for example:
  ```java
    interface Test {
      void test();
    }
    Test t = new Test() {
      @Override
      public void test() { }
    };  // don't forget the semi-colon!
    t.test();
  ```
  2. _Anonymous classes_ can be used to flexibly create inline instances that perform certain tasks the caller defines. Please review the lecture on [10/15/2020 - "Uses for Anonymous Classes"](https://cs125.cs.illinois.edu/lessons/anonymousclasses/#uses-for-anonymous-classes).
##### Practice 3
---

#### Lambda Expression
  1. **Functional programming** is a style of programming for which programs are constructed by applying and composing functions, while **object-oriented programming** (e.g. Java) is a style for which programs are constructed by manipulating objects.
  2. Java cannot store functions in variables (as opposing to what functional programming). However, Java can achieve some similar expression style called **lambda expression**. For example:
  ```java
    interface Increment {
      int increment(int value);
    }
    // method 1 - using anonymous class
    Increment a = new Increment() {
      @Override
      public int increment(int value) {
        return value + 1;
      }
    };
    // method 2 - using lambda expression
    Increment b = (value) -> value + 1;

    // the following codes both print 11
    System.out.println(a.increment(10));
    System.out.println(b.increment(10));
  ```
##### Practice 4
---


### Combining it all together!
