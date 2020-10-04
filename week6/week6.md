# Quiz Preparation for Week 6

_**function and method**: interchangable_

_**variable and field**: interchangable_

_**instance and object**: interchangable_

### Concepts
  * [Static function/variable](#static-function/variable) (09/28)
  * [Inheritance](#inheritance) (09/29)
    - overriding functions
  * [Polymorphism](#polymorphism) (09/30)
    - "is a" relationships
    - up/down casting
  * [Equality and Copy Constructor](#equality-and-copy-constructor) (10/01)
    - overriding equals()
    - designing copy constructor

### Warm-ups problems
##### Static function/variable
  1. What is a **static function** for a class? What's its difference from an **instance function**?
  2. A static function can/cannot do ______?
  3. What does keyword _final_ do?

##### Inheritance
  4. **Bird** is a type of **animal**. A **chick** is a bird. A **penguin** is a bird. Declare four classes to reflect their relationships.
  5. What is the keyword for invoking parent class constructor?
  6. Given the following class declarations, what variable(s) can **Bird** access from **Animal**?
  ```java
  public class Animal {
    public int one;
    private int two;
    protected int three;
  }
  public class Bird extends Animal {
    // things
  }
  ```
  7. How do you override a function from the parent class?

##### Polymorphism
  8. Identify the error in the following codes:
  ```java
  public class Bird { }
  public class Penguin extends Bird { }

  void isPenguin(Penguin d) { /* do nothing */}

  Bird b = new Bird();
  isPenguin(b);
  ```
  9. What is upcasting? Given the following codes, what can **Penguin** be upcast to?
  ```java
  public class Animal { }
  public class Bird extends Animal { }
  public class Penguin extends Bird { }
  ```

  10. Assume we have the following codes, will there be an error? Why?
  ```java
    public class Penguin extends Bird {
      public void swim() {}
    }

    Bird b = new Penguin();
    b.swim();
  ```

  11. Assume we have the following codes, will there be an error? Why? _(Hint: this is about down casting)_
  ```java
    public class Penguin extends Bird {
      public void swim() { }
    }

    Bird b = new Penguin();
    if (b instanceof Penguin) {
      Penguin thisB = (Penguin) b;
      thisB.swim();
    }
  ```

##### Equality and Copy Constructor
  12. What are some aspects you want to check for designing your **equals()** function?

  13. How do you define a copy constructor?

### Combining it all together!
Whew! That's a lot of materials above huh?
