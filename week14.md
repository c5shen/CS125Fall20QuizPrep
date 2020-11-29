# Quiz Prep Week 14 

### Concepts
* [Bubble Sort](https://cs125.cs.illinois.edu/lessons/sorting/#bubble-sort)
* [Insertion Sort](https://cs125.cs.illinois.edu/lessons/sorting/#insertion-sort)
* [Merge Sort](https://cs125.cs.illinois.edu/lessons/mergesort/)
* [Quick Sort](https://cs125.cs.illinois.edu/lessons/quicksort/)
* [Binary Search](https://cs125.cs.illinois.edu/lessons/binarysearch/)

### EMP Session Links 
* [EMP 11-17](https://cs199emp.netlify.app/dist/2020-11-19.html)

### Concept Overview and Practice

1) Create a public class named Sorter and add the following functions
  
  a) Create a static method named bubbleSort, that takes in an array of Comparables and sorts them using bubble sort. 
    <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter {
    
    public static void bubbleSort(Comparable[] arr) {
      int n = arr.length; 
      for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
          if (arr[j].compareTo(arr[j + 1]) > 0) { 
            Comparable temp = arr[j]; 
            arr[j] = arr[j + 1]; 
            arr[j + 1] = temp; 
          } 
        }
      }
      return arr;
    }
  }
   ```
  </details>
  <br></br>
  
