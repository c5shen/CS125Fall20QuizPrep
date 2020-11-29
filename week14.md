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
  
  a) Create a static method named bubbleSort, that takes in an array of Comparables and sorts them using bubble sort and returns the sorted array. 
    <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter {
    
    public static Comparable[] bubbleSort(Comparable[] arr) {
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
  
  b) Create a static method named insertionSort, that takes in an array of Comparables and sorts them using insertion sort and returns the sorted array.
    <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter {
    
    public static Comparable[] bubbleSort(Comparable[] arr) {
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
  public static Comparable[] insertionSort(Comparable[] arr) {
      int n = arr.length; 
      for (int i = 1; i < n; ++i) { 
        Comparable key = arr[i]; 
        int j = i - 1; 
        while (j >= 0 && arr[j].compareTo(key) > 0) { 
          arr[j + 1] = arr[j]; 
          j = j - 1; 
        } 
        arr[j + 1] = key; 
      }
      return arr;
    }
 }
   ```
  </details>
  <br></br>
  
  c) Create a static method named mergeSort, that takes in an array of ints, and sorts them using merge sort and returns the sorted array. This function also takes in an int start, and an int end. (Hint: Your class may need to extend Merge)
  <details>
   <summary>Spoiler!</summary>

   ```Java
   public class Sorter extends Merge{
    
    public static Comparable[] bubbleSort(Comparable[] arr) {
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
  public static Comparable[] insertionSort(Comparable[] arr) {
      int n = arr.length; 
      for (int i = 1; i < n; ++i) { 
        Comparable key = arr[i]; 
        int j = i - 1; 
        while (j >= 0 && arr[j].compareTo(key) > 0) { 
          arr[j + 1] = arr[j]; 
          j = j - 1; 
        } 
        arr[j + 1] = key; 
      }
      return arr;
    }

 public static int[] mergeSort(int[] arr, int start, int end) {
      if (end - start < 2) {
          int[] res = {arr[start]};
          return res;
        }
        int mid = (start + end) / 2;
        int[] left = mergeSort(arr, start, mid);
        int[] right = mergeSort(arr, mid, end);
        return merge(left, right);
     }
}
   ```
  </details>
  <br></br>

