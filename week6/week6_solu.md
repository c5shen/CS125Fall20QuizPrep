### Warm-ups solutions
1.
  - A **static function** is a type of function that you invoke without creating an instance of the class. For example, we have a class named **MyClass** with a static function **public static void foo()**. Then, we can call it by **MyClass.foo()**.
  - An **instance function** can only be called by an instance of the class. For example, you have an instance **MyClass c = new MyClass()** and a instance function **public void bar()**. Then, we can call it by **c.bar()**.

2. A static function cannot access/modify **instance variables** of the class, but it can access/modify **static variables** of the class.

3. It marks a variable to be unchangable after being set.

4.  ```java
    public class Animal { }
    public class Bird extends Animal { }
    public class Chick extends Bird { }
    public class Penguin extends Bird { }
    ```
5. The keyword is **super**. Depending on your constructor(s) defined in the parent class, super can have different numbers of parameters.

6. _one_ and _three_.

7. By using the `@Override` label and having the same function declaration of the parent function.
