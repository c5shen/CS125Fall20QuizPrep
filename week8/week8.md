# Quiz Preparation for Week 8

### Concepts
  * [Abstract](#abstract)
  * [Interface](#interface)
  * [Anonymous Class](#anonymous-class)
    - Usage with other class
    - Usage with interface
  * [Lambda Expression](#lambda)

### Quick Concept Overview
##### Abstract
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

##### Interface
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

##### Anonymous Class


##### Lambda


### Warm-ups problems
##### Abstract


##### Interface


##### Anonymous Class


##### Lambda


### Combining it all together!
