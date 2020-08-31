# Quiz Preparation for Week 0

### Concepts
  * Variables/Types
  * Operations
  * Conditional Expressions/Statements

### Warm-up problems
1. What variable type would you (most likely) use if you want to store **a student's midterm score**?
    - what about **GPA**?
2. Think about how to add **1 point extra credit** to an existing variable named _midtermScore_.
    - Now, think about how to apply a **10%** penalty to an existing variable named _hw1_.
3. How would you check if _finalScore_ passes an A cutoff of **90**?
4. How do you know if a student gets **As** on all homework assignments (e.g. _hw1_, _hw2_,...)?

### Combine them altogether!
#### You are taking a course taught by Dr. Evil.
People call him Dr. Evil for a reason: he is unmerciful on grading, and you will be thrown into a dungeon for 3 days if you fail his course. What's worse, he asks you -- yes YOU -- to do the grading for him, including your own (of course, he will definitely know if you make any, "unintentional" changes).

You wrote 3 homework assignments and took one midterm exam. On homework 1, you got **87** out of 100; on homework 2, you got lucky and hit **93**; on homework 3, you slacked a bit and sadly swallowed a score of **82**. Fortunately, your midterm grade is fair, which is **90.5**.

    1. How would you store these score?
<details>
  <summary>Spoiler!</summary>

  ```java
    // If you like percentage more
    //int hw1 = 87;
    //int hw2 = 93;
    //int hw3 = 82;
    //double midtermScore = 90.5;

    // or if you like fraction more
    double hw1 = 0.87;
    double hw2 = 0.93;
    double hw3 = 0.82;
    double midtermScore = 0.905;
  ```
</details>
<br></br>

Now Dr. Evil announced that each of your homework weighs **10%** of your total grade, and your midterm weighs **30%**. That means your final will contribute **40%** to your grade, phew! Supposedly you got **93** on your final exam.

    2. What's your total grade, numerically?
<details>
  <summary>Spoiler!</summary>

  ```java
    // using fraction
    double finalScore = 0.93;
    double hwAverge = (hw1 + hw2 + hw3) / 3;
    double totalGrade = 0.3 * hwAverage + 0.3 * midtermScore + 0.4 * finalScore;
  ```
  Numerically `totalGrade = 0.9015`.
</details>
<br></br>

While now is the tricky part. You somehow actually got 93 on your final. You are glad because you think your total is roughly at the A cutoff.

    3. If the A cutoff is 0.90 (greater than or equal to 0.90 and you get an A), will you get it?
<details>
  <summary>Spoiler!</summary>

  ```java
    // store the information in a boolean
    boolean getA = totalGrade >= 0.90;
    if (getA) {
      System.out.println("Haha! I get A!");
    } else {
      System.out.println("Oops not an A.");
    }
  ```
  Yes, you get an A!
</details>
<br></br>

Come on, you know Dr. Evil won't let you easily walk away from his course! Dr. Evil asserts that in his course, there will be only A or F. In addition, you have to get **at least 0.85** on _hw3_, or you get a **2%** penalty from your final score (not total!). What's even more, your final score itself needs to be **at least 0.90** to get an A. However, Dr. Evil shows a tiny bit of mercy, saying that
  > "If your **homework average is at least 0.85**, then even if your final is not at least 0.90, you can still get an A."

    4. What's your total grade now? Will you be thrown into the dungeon for failing the course, despite all the efforts?
<details>
  <summary>Spoiler!</summary>

  ```java
    // get updated final
    if (hw3 < 0.85) {
      finalScore *= 0.98;
    }
    totalGrade = 0.3 * hwAverage + 0.3 * midtermScore + 0.4 * finalScore;

    // see if you will be thrown to the dungeon
    if (totalGrade >= 0.90) {
      if (finalScore >= 0.90 || hwAverage >= 0.85) {
        System.out.println("Finally, an A!");
      } else {
        System.out.println("It's. Just. Brutal...");
      }
    } else {
      System.out.println("Well, maybe I can do better.");
    }
  ```
  Since your _hw3_ is 0.82, you suffer a 2% penalty on final. Hence, you `finalScore = 0.9114`. However, now your `totalGrade = 0.89806`. Dungeon you go!
</details>
