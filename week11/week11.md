# Quiz Prep Week 11

### Concepts
  ####  Concepts covered in week 8 review (refer to [that](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week9/week9.md) for practice)
  * Big-O Notation
  * Type Parameters
  * Array List
  * Linked List
  * Inner Class

  ####  Concepts covered in week 9
  * [Hashing](https://cs125.cs.illinois.edu/lessons/hashing/#java's-hashcode)
  * [Maps](https://cs125.cs.illinois.edu/lessons/maps/)
  
  #### Concepts covered in Week 10
  ##### Exceptions
   - [Catching](https://cs125.cs.illinois.edu/lessons/catchingexceptions/)
   - [Throwing](https://cs125.cs.illinois.edu/lessons/throwingexceptions/)
   - [Working with Exceptions](https://cs125.cs.illinois.edu/lessons/workingwithexceptions/)
  

### EMP Session Links

1) [EMP 10-29](https://cs199emp.netlify.app/dist/2020-10-29.html)
2) [EMP 11-05](https://cs199emp.netlify.app/dist/2020-11-05.html)

### Internet theoretical questions
1. Is the internet primarily wired or wireless?

  <details>
  <summary>Spoiler!</summary>
 
  #### Wired. Your laptop or phone may be wireless but they just connect to access points and the rest of the international internet is wired because it's far more energy efficient, reliable and cheaper.
  
  </details>
  <br></br>

2. What are different types of cables that make up the internet? How do we decide which ones to pick?
  <details>
  <summary>Spoiler!</summary>
 
  #### Many different cables exist. In class we looked at twisted pair CATV coaxial cables and glass based fibre optic cables. We decide based on the range we want (100m or kilometres), cost of cabling, bandwidth and speed. 
  
  </details>
  <br></br>

3. Why do we have internet protocols? Who implements these protocols?
  <details>
  <summary>Spoiler!</summary>
 
  #### We need internet protocols because computers are bad at inferring what the incoming data (packets) is by context, so we define the structure of the packet and what to do with it. The protocols are just a set of rules (like interfaces) and it's up to the programmer to implement.
  
  </details>
  <br></br>

4. Let's say I have a phone which I use to open Wikipedia on my Firefox browser, which is the server and which is the client?
  <details>
  <summary>Spoiler!</summary>
 
  #### The phone running firefox is the client and Wikipedia has the server (in practice they have a giant cluster of them).
  
  </details>
  <br></br>

5. What is an I.P Address? What is your current IP Address? What information does it have?
  <details>
  <summary>Spoiler!</summary>
 
  #### IP Addresses are a unique identifier of computers within a network. The address can indicate a lot about your location and where you are connecting as well.
  
  </details>
  <br></br>

6. When do we use `GET` and when do we use `POST`?
  <details>
  <summary>Spoiler!</summary>
 
  #### We use `GET` when we want to recieve data (for example a news article or online profile) and `POST` when we want to send data (like creating a new news article or updating your online profile)
  
  </details>
  <br></br>

### Concept Overview & Practice

1) Assuming there is class Laptop that contains a constructor that takes in one String input which is the name of the company, then consider the segment of code below: 
  ```Java
   Laptop a = new Laptop("Apple");
   Laptop b = new Laptop("Apple");
   Laptop c = new Laptop("Microsoft");
   
   System.out.println(a.hashCode()); // Line 1
   System.out.println(b.hashCode()); // Line 2
   System.out.println(c.hashCode()); // Line 3
  ```
  Which two lines will print the same output?
  
  <details>
  <summary>Spoiler!</summary>
 
  #### Neither. Since a,b and c are all different instances, they'll all have a unique hashcode!
  
  </details>
  <br></br>
  
  2) What Java objects have access to the built-in hashcode function?
  <details>
   <summary>Spoiler!</summary>
 
   #### All of them!
  
  </details>
  <br></br>
  
  3) Write a function named oddOrEven that takes in an array of integer inputs and maps them to a True or False value based on whether its even or odd respectively. This function should return this map.
  <details>
   <summary>Spoiler!</summary>
 
   ```Java
   public Map<Integer, Boolean> oddOrEven(int[] arr) {
      Map<Integer, Boolean> map = new HashMap<>();
      for (int i : arr) {
         if (i % 2 == 0) {
          map.put(i, true);
         } else {
            map.put(i, false);
         }
      return map;
    }
          
           
   ```
  </details>
  <br></br>
  
  4) Write a function named fractions, which takes in two int arrays of the same length and returns and array of integers that has the values from the first array divided by second. (Keep in mind that when you divide a number by 0 java will throw an ArithmeticException, so you should take care of that!)
   <details>
   <summary>Spoiler!</summary>
 
   ```Java
   public int[] fractions(int[] a, int[] b) {
      assert a != null && a.length != 0 && b != null && b.length != 0;
      int[] output = new int[a.length]; //or b.length
      try {
         for (int i = 0; i < a.length; i++) {
            output[i] = a[i]/b[i];
         }
         return output;
      } catch (ArithmeticException e) {
          System.out.println("Cannot divide by zero!");
      }
      }
                
           
   ```
  </details>
  <br></br>
  
  5) Write a function isAscending that takes in an int array, and returns true if the array is in ascending order, but throws an IllegalArgumentException otherwise
   <details>
   <summary>Spoiler!</summary>
 
   ```Java
   public boolean isAscending(int[] arr) {
      assert arr != null && arr.length != 0;
      for (int i = 0; i < arr.length - 1; i++) {
        if (arr[i] > arr[i+1]){
         throw new IllegalArgumentException("Array is not ascending");
        }
      }
      return true;
    }   
   ```
  </details>
  <br></br>
