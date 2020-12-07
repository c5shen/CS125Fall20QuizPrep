# Quiz(Midterm 2) Prep Week 15

### Concepts for week 15 (will not be on the midterm)
  * Generics
  * Streams
  * Kotlin! (optional)

### Other topics for this midterm
  * Big-O, Type parameters, ArrayList/LinkedList, Inner class (see [week 9 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week9/week9.md))
  * Hashing, Maps, Exceptions, Internet Stuff (see [week 11 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week11/week11.md))
  * Recursion, Trees (see [week 12 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week12/week12.pdf))
  * Sorting algorithms, Binary Search (see [week 14 review](https://github.com/c5shen/CS125Fall20QuizPrep/blob/master/week14/week14.md))

### EMP Session Links

See week9-14 review for EMP practice links.

## We will be doing Q&A after today's material!

### Older content review Reivew

1. What makes Binary Search so efficient? What is the Big-O complexity of it?
<details>
  <summary>Spoiler!</summary>
  It divides the space into half again and again making the steps equal to log_2 of the size. In big O that's O(log n).
</details>

2. Suppose you have an unsorted array and you want to search through all the items. Would it be better to do a linear search (for loop through all items) or sort and then take advantage of a binary search? Answer this in terms of Big O.
<details>
  <summary>Spoiler!</summary>
  Linear search is O(n) and much better in almst every case. Binary research is O(log n) but sorting is O(n log n) making the overall complexity of the other approach O(n log n). However if you're lucky and the array is nearly sorted then this might be faster. Also if you have to search lots and lots of times it might be better to sort once so that each time the search can be more efficient.  
</details>

3. Write a program that sums the left most value and the right most value of a tree. What is the Big O complexity of this? Can you do this iteratively and recurisvely?

### Generics
1. What is a classic usage of generic in Java (_Hint: you put items in it, you can extend it or shrink it, ..._)?
<details>
  <summary>Spoiler!</summary>
  List, Tree, Map etc.
</details>

2. What are the conventional names of generics for number/element/key/value? (_Hint: This is how it appears on Java doc_)
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

<details>
<summary>Spoiler!</summary>
More succinct, composable, efficient. Can be parallelized.
</details>

### Tree question answer

Iterative:

```java
// barebones tree for example, your quiz/midterm uses more complicated stuff
class Tree {
  int value;
  Tree left;
  Tree right;
}
int sum(Tree t) {
  int leftVal = 0;
  Tree treeLeft = t.left;
  while (treeLeft != null) {
    leftVal = treeLeft.value;
    treeLeft = treeLeft.left;
  }
  
  int rightVal = 0;
  Tree treeRight = t.right;
  while (treeRight != null) {
    rightVal = treeRight.value;
    treeLeft = treeRight.left;
  }
  
  return leftVal + rightVal;
}
```

Recursive:
```java
int sum(Tree t) {
  int leftVal = leftVal(t);
  int rightVal = rightVal(t);
  
  return leftVal + rightVal;
}

int leftVal(Tree t) {
  if (t.left == null) {
    return t.value;
  } 
  return leftVal(t);
}

int rightVal(Tree t) {
  if (t.right == null) {
    return t.value;
  }
  return rightVal(t);
}
```

### Kotlin

To learn more about Kotlin checkout [CS 199: Intro to Kotlin Programming](https://kotlin.cs.illinois.edu/) and [Gentle Kotlin](https://gentlekotlin.com/cheatsheet). Harsh was the only staff when the course started last Spring and he'll be glad to answer. See you all there hopefully next semester!
