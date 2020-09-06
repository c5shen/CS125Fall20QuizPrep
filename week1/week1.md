# Quiz Preparation for Week XXX

### Concepts
  * Arrays
  * Loops
  * Algorithms I
  * Functions


### Warm-ups problems
  1. How would you create an array of the **first 5 even numbers**?
  2. Consider another array, with 5 numbers (you don't know which numbers), how would you calculate the **sum of these 5 numbers**?
  3. Consider the same array from question 2, write a short algorithm to check, if the number 7 is the array, and print "Found 7!" if it is, and "Did not find 7" otherwise.
  4. Write a function named product, that takes two int inputs, and returns the **product** of these two inputs.

### Combining it all together!
#### Dr. Evil is back!
So Dr. Evil is once again making you do all the hard work. He has your scores for all the exams you have taken in his course saved in four **double** variables named **midterm1**, **midterm2**, **midterm3** and **final**

1. How would you store these scores in an array named **scores**?
<details>
  <summary>Spoiler!</summary>

  ```java
      double scores[] = {midterm1, midterm2, midterm3, final};
  ```
</details>
<br></br>

So now Dr. Evil has just announced that, if any of these scores, fall below **80.0%** you automatically fail the class (sooo evil right?).

2. Write code to check to see if you fail the class based on the conditions above. Print "Oops, I failed!" if you do.
<details>
  <summary>Spoiler!</summary>

  ```java
      for (int i = 0; i < scores.length; i++) {
        if (scores[i] < 80.0) {
          System.out.println("Oops, I failed");
        }
       }
       
       //or
       
       int i = 0;
       while (i < scores.length) {
        if (scores[i] < 80.0) {
          System.out.println("Oops, I failed");
        } 
        i++;
       }
  ```
</details>
<br></br>

Dr Evil now feels that he has been too evil, so he offers 1% extra credit to be nice, but he not really that nice, because he says that you only get extra-credit if you have a **perfect score (100.0%)** on any of those exams!

3. How will you check if you get that 1% e.c? Print "Yay" if you do
<details>
  <summary>Spoiler!</summary>

  ```java
      for (int i = 0; i < scores.length; i++) {
        if (scores[i] == 100.0){
          System.out.println("Yay");
         }
        }
  ```
</details>
<br></br>

Now obviously, since you're worried about your average in this class. You decide to write a function that calculates average.

4. Write a function called **average** that takes an arbitrary double array, and returns the average of all elements in that array. After doing that call this function using your scores array from above as an input for this function and print the average.
<details>
  <summary>Spoiler!</summary>

  ```java
      double average(double[] arr) {
        double sum = 0;
        for (int i = 0; i < arr.length; i++) {
          sum += arr[i]; // you can also do sum = sum + arr[i];
        }
        return sum/arr.length;
       }
       
       System.out.println(average(scores));
  ```
</details>
<br></br>
