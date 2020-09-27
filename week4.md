# Quiz Preparation for Week 4

### Concepts
  * Objects
  * Constructors
  * Encapsultion


### Warm-ups problems
  1. What is an object in Java?
  2. What is a Constructor?
  3. How many constructors can a class have? What does constructor overloding mean?
  3. What does Encapsulation mean?

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
        public String getGPA() {
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
        public void getGPA(double g) {
          gpa = g;
        }
      }
  ```
</details>
<br></br>
