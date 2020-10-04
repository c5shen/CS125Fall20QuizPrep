### Warm-ups solutions
1.
  - A **static function** is a type of function that you invoke without creating an instance of the class. For example, we have a class named **MyClass** with a static function **public static void foo()**. Then, we can call it by **MyClass.foo()**.
  - An **instance function** can only be called by an instance of the class. For example, you have an instance MyClass c = new MyClass()** and a instance function **public void bar()**. Then, we can call it by **c.bar()**.

2. A static function cannot access/modify **instance variables** of the class, but it can access/modify **static variables** of the class.

3. It marks a variable to be unchangable after being set.

4.
  ```java
    public class Animal { }
    public class Bird extends Animal { }
    public class Chick extends Bird { }
    public class Penguin extends Bird { }
  ```
5. The keyword is **super**. Depending on your constructor(s) defined in the parent class, super can have different numbers of parameters.

6. _one_ and _three_.

7. By using the `@Override` label and having the same function declaration of the parent function.

8. The function call will throw an incompatible type error: because a Pet is not necessarily a Penguin.

9. Upcasting is referring to an object to its supertypes. A few examples:
  ```java
  Penguin p = new Penguin();
  Bird b = new Penguin();   // upcasting to Bird
  Animal a = new Penguin(); // upcasting to Animal
  Object o = new Penguin(); // upcasting to Object
  ```
  The functions/variables available for the object to use is determined by the type it is cast to. For example, **a** cannot access functions/variables uniquely defined in the Penguin class because it has type **Bird**.

10. Yes, because **b** has no access to function **swim()** as it has type **Bird**.

11. No, because we downcast **b** to be Penguin and so it can access Penguin class function. This is doable for **b** because it is an instance of Penguin at the first place (although we upcast it to Bird type first).

12. If the object comparing to is _null_; if it is an instance of the current object; anything else you think that should be equal.

13. For example:
  ```java
  public class Animal {
    // any variables defined

    public Animal() { }

    public Animal(Animal other) {
      // copy over the variables "other" has
    }
  }
  ```
