# Quiz Preparation for Week 5

### Concepts
  * Objects
  * Constructors
  * Encapsultion


### Warm-ups problems
  1. What is an object in Java?
  2. What is a Constructor?
  3. How many constructors can a class have? What does constructor overloding mean?
  4. What does Encapsulation mean?
  5. What are private variables and how do we read and write them?
  6. How would you define a getter and setter for a field called `firstName`?
  7. What is the mistake in this code? 
  
    ```java
    public class Course {
      private String name;
      private int number;
      public Course(String nameNew, int num) {
        nameNew = name;
        num = number;
      }
    }
    ```
 8. Lets say you have to model a `Triangle` in Java and add a function for it's perimeter. What will be your variables and what will be your functions? Don't worry about getters and setters on this one. 

### Combining it all together!
We are going to define a class named GradeReport.
  1. Define a class named GradeReport. Your class should store two **private** variables **name** and **gpa**
  <details>
  <summary>Spoiler!</summary>

  ```java
      public class GradeReport {
        private String name;
        private double gpa;
      }
  ```
</details>
<br></br>
  2. Add a constructor to your class definition that takes in two parameters: a name and a gpa value, and sets the stored values of name and gpa to the values in the parameters
  <details>
  <summary>Spoiler!</summary>

  ```java
      public class GradeReport {
        private String name;
        private double gpa;
        public GradeReport (String n, double g) {
          //you can add assert statements to check for invalid inputs, but for now we are just going to assume these are valid.
          name = n;
          gpa = g;
        }
      }
  ```
</details>
<br></br>
  3. Add a getName and a getGPA function that returns the name and gpa values respectively
  <details>
  <summary>Spoiler!</summary>

  ```java
      public class GradeReport {
        private String name;
        private double gpa;
        public GradeReport (String n, double g) {
          //you can add assert statements to check for invalid inputs, but for now we are just going to assume these are valid.
          name = n;
          gpa = g;
        }
        public String getName() {
          return name;
        }
        public double getGPA() {
          return gpa;
        }
      }
  ```
</details>
<br></br>
  4. Add two functions setName and setGPA that take in a parameter for a name and gpa respectively and change the value of name and gpa respectively. These functions don't return anything.
   <details>
  <summary>Spoiler!</summary>

  ```java
      public class GradeReport {
        private String name;
        private double gpa;
        public GradeReport (String n, double g) {
          //you can add assert statements to check for invalid inputs, but for now we are just going to assume these are valid.
          name = n;
          gpa = g;
        }
        public String getName() {
          return name;
        }
        public double getGPA() {
          return gpa;
        }
        public void setName(String n) {
          name = n;
        }
        public void setGPA(double g) {
          gpa = g;
        }
      }
  ```
</details>
<br></br>
