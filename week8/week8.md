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
  5. An _abstract method_ doesn't have a body (the brackets), e.g.:
  ```java
    public abstract class Circle {
      public abstract int radius();
    }
  ```

##### Interface


##### Anonymous Class


##### Lambda


### Warm-ups problems
##### Abstract
  1. Can be applied to both classes and methods, e.g.:
  ```java
    public abstract class Shape {
      public abstract int sides();
    }
  ```

##### Interface


##### Anonymous Class


##### Lambda


### Combining it all together!
