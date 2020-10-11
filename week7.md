## Topics
1) References
2) Polymorphism
3) Memory Management
4) Imports and Libraries
5) Serialization

## Practice Problem 
* Define a class named Thing with two *private fields*, a String *name* and a String *type*. 
* Create a *public constructor* with two String inputs that update the values of these fields. 
* Create a public class method isReference that takes in two Thing objects, and returns *True* only if both references are equal. You should *assert* that your objects are not null. 
* Write a function named Copy that takes in an array of Things and returns an array containing two Things arrays, one with a shallow copy of all the elements in the input array and another that returns a deep copy of all the elements in the input array. (So, your function should return a 2D array). (Assume that Thing has an existing copy constructor)
* Right a function named randomThings that takes in an array of Thing and prints out (does not return!)4 random "things" from that array.(You might wanna import a library for this)

## Solution
<details>
  <summary>Spoiler!</summary>

  ```java
      import java.util.Random
      public class Thing {
         private String name;
         private String type;
         public class Thing (String n, String t) {
          name = n;
          type = t;
         }
         public static boolean isReference(Thing a, Thing b) {
          assert a != null;
          assert b != null;
          
          return a == b;
         }
         public Thing[][] copy(Thing[] arr) {
          assert arr != null;
          Thing[] shallow = new Thing[arr.length];
          Thing[] deep = new Thing[arr.length];
          for (int i = 0; i < arr.length; i++) {
            shallow[i] = arr[i].clone();
            deep[i] = new Thing(arr[i]);
          }
          Thing[][] output = {shallow, deep};
          return output;
          }
          public void randomThings(Thing[] arr) {
            //You will tell me this step by step
           }
          
      }
  ```
</details>
<br></br>
