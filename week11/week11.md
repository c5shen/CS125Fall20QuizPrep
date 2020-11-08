# (Quiz)Midterm Preparation for Week 11

### Concepts
  * Concepts covered in week 9 review
  * [Hashing](https://cs125.cs.illinois.edu/lessons/hashing/#java's-hashcode)
  * [Maps](https://cs125.cs.illinois.edu/lessons/maps/)
  
  * Concepts covered in Week 10
  * Exceptions
   - [Catching](https://cs125.cs.illinois.edu/lessons/catchingexceptions/)
   - [Throwing](https://cs125.cs.illinois.edu/lessons/throwingexceptions/)
   - [Working with Exceptions](https://cs125.cs.illinois.edu/lessons/workingwithexceptions/)
  

### EMP Session Links

1) [EMP 10-20](https://cs199emp.netlify.app/dist/2020-10-29.html)
2) [EMP 11-05](https://cs199emp.netlify.app/dist/2020-11-05.html)


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
           
   ```
  </details>
  <br></br>
