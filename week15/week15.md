# Quiz(Midterm 2) Prep Week 15

### Concepts for week 15
  * Generics
  * Streams
  * Kotlin! (optional)

### Other topics for this midterm
  * Big-O, Type parameters, ArrayList/LinkedList, Inner class (see [week 9 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week9/week9.md))
  * Hashing, Maps, Exceptions, Internet Stuff (see [week 11 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week11/week11.md))
  * Recursion, Trees (see [week 12 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week12/week12.pdf))
  * Sorting algorithms, Binary Search (see [week 14 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week14/week14.md))

### EMP Session Links


## We will be doing some prior material review and Q&A after today's material!


### Generics
1. What is a classic usage of generic in Java (_Hint: you put items in it, you can extend it or shrink it, ..._)?
<details>
  <summary>Spoiler!</summary>
  List
</details>

2. What are the conventional names of generics for number/element/key/value?
<details>
  <summary>Spoiler!</summary>
  N for number, E for element, K/V for key and value (in maps)
</details>

3. How do we change the following class definition to use generics?
```Java
public class MyList {
  private List<Object> list;
  private int size;
  public MyList(int setSize) {
    size = setSize;
    list = new ArrayList(setSize);
  }
}
```
<details>
  <summary>Spoiler!</summary>

```java
public class MyList<E> {
  private List<E> list;
  private int size;
  public MyList(int setSize) {
    size = setSize;
    list = new ArrayList(setSize);
  }
}
```
</details>

4. Can you implement generics on array in Java?
<details>
<summary>Spoiler!</summary>
No! Java array needs to have a specific type.
</details>


### Streams
1. Convert the following for loop to stream.
```java
int count = 0;
for (int i = 0; i < 5; i++) {
  if (i % 3 == 0) {
    count += 1;
  }
}
```
<details>
<summary>Spoiler!</summary>

```Java
int count = Stream.of(1, 2, 3, 4, 5)
  .filter(e -> e % 3 == 0)
  .count();
```
</details>

2. What does the following stream do?
```Java
int mystery = Stream.of(1, 2, 3, 4, 5)
  .filter(e -> e % 3 != 0)
  .reduce(1, (a, b) -> a * b);
System.out.println(mystery);
```
<details>
<summary>Spoiler!</summary>
It returns the product of all the inputs that are not multiples of 3, which is 40.
</details>

3. Why do we use Streams?

More succinct, composable, efficient.
