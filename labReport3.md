# Part 1 - Bugs
## 1. A Failure-Inducing Input for the Buggy Program
Failure Inducing Input: 
```
@Test
 public void testReversed() {
   int[] input = {29, 10, 11};
   int[] expected = {11, 10, 29};
   ArrayExamples.reversed(input);
   assertArrayEquals(expected, input);
 }

```
Associated Code: 
```
public class ArrayExamples {

 static int[] reversed(int[] arr) {
   int[] newArray = new int[arr.length];
   for(int i = 0; i < arr.length; i += 1) {
     arr[i] = newArray[arr.length - i - 1];
   }
   return arr;
 }
}
```

## 2. An Input that Doesn't Induce a Failure
Non-Failure Inducing Input: 
```
@Test
 public void testReversed2() {
   int[] input = {1, 10, 100, 1000};
   int[] expected = {1000, 100, 10, 1};
   assertArrayEquals(expected, ArrayExamples.reversed(input));
 }
```
Associated Code: 
```
public class ArrayExamples {

 static int[] reversed(int[] arr) {
   int[] newArray = new int[arr.length];
   for(int i = 0; i < arr.length; i += 1) {
     newArray[i] = arr[arr.length - i - 1];
   }
   return newArray;
 }
}
```

## 3. The Output of Running the Two Tests Above
Failure Output: 
![Screenshot](labReport3FailureOutput.png)
Success Output: 
![Screenshot](labReport3SuccessOutput.png)


## 4. The Bug (Code that Required to Fix It)
The bug was incorrect update of the element of the array and incorrect return array. 

Inccorect Code: 
```
public class ArrayExamples {

 static int[] reversed(int[] arr) {
   int[] newArray = new int[arr.length];
   for(int i = 0; i < arr.length; i += 1) {
     arr[i] = newArray[arr.length - i - 1];
   }
   return arr;
 }
}
```
- The code above updates the value to the input array (arr). 

Correct Code: 
```
public class ArrayExamples {

 static int[] reversed(int[] arr) {
   int[] newArray = new int[arr.length];
   for(int i = 0; i < arr.length; i += 1) {
     newArray[i] = arr[arr.length - i - 1];
   }
   return newArray;
 }
}
```
- The code above updates the value to the newly created array (newArray).

## 5. Briefly Describe Why the Fix Addresses the Issue
The code before fixing it updated the input array with the values of the new array. Considering that the new array was filled with initial integer value 0 for input array length amount, elements of the input array were updated to 0. However, the fixed code updates the elements of the new array with elements of the input array in reverse order and returns the updated new array. 
