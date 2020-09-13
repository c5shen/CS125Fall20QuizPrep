### Warm-ups solutions
  1. Functions defined by the same name but different parameters (NOTICE: not by different return type!).
  2. No. the type of function `foo(int, int)` has been defined already.
  3. ```java
      int len = theString.length()
      ```
  4. ```Java
      String newString = foo + "?" + bar;
      ```
  5. the object is uninitialized.
  6. ```java
      if (object == null) {
        // do something
      }
      ```
  7. It will give you an error on lossy conversion from **double** to **int**.
  8. examples:
      - mutable: **int, double, ...**
      - immutable: **String**, all Wrapper classes (not necessary for the quiz)...
  9. ```Java
      String a = "I have\nan\napple";
      String[] out = a.split("\n");
      ```
  10. You want to make sure uninitialized variables are not referred to accidentally (bad bad!).

### Example codes for the practice
##### 1. Parsing the data
```Java
String[] parsedSales = sales.split("\n");
```

##### 2. Check for errors
```Java
// 1. lazy way for this question
boolean checkErrors(String[] a, String[] b) {
  // if both arrays are null, no errors
  if (a == null && b == null) {
    return true;
  }
  // if either array is null, then return false
  if (a == null || b == null) {
    return false;
  }

  int totalNumGame = a.length;
  for (int i = 0; i < totalNumGame; i++) {
    if (!a[i].equals(b[i])) {
      return false;
    }
  }
  return true;
}

/*
...
*/

// 2. split String again and compare sale/percentage changes
//    by their corresponding values
boolean checkErrors(String[] a, String[] b) {
  // if both arrays are null, no errors
  if (a == null && b == null) {
    return true;
  }
  // if either array is null, then return false
  if (a == null || b == null) {
    return false;
  }

  int totalNumGame = a.length;
  for (int i = 0; i < totalNumGame; i++) {
    String[] itemA = a[i].split(",");
    String[] itemB = b[i].split(",");
    double saleA = Double.parseDouble(itemA[1]);
    double saleB = Double.parseDouble(itemA[2]);
    double percentA = Double.parseDouble(itemB[1]);
    double percentB = Double.parseDouble(itemB[2]);
    if (saleA != saleB || percentA != percentB) {
      return false;
    }
  }
  return true;
}
```

##### 3. Report to GabeN
```Java
void report(String sale) {
  String[] parsedSale = sale.split(",");
  String filler1 = " total sale is $";
  String filler2 = " mil. Comparing to last week, it changes ";
  String filler3 = "%.";
  System.out.println(parsedSale[0] + filler1 + parsedSale[1]
  + filler2 + parsedSale[2] + filler3);
}
```
