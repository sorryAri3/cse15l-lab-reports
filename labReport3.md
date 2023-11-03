# LAB REPORT 3 #

## Symptoms and Failure- Inducing Inputs using Array Methods ##

The bug I am choosin for this lab report is the `reversedInPlace` bug.

### The failure inducing input

```
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {3,4,5,6,7 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{7,6,5,4,3 }, input1);
	}
```

### TEST CODE 
``` public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```


### The success inducing input

```
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {3,4,5,6,7 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{7,6,5,4,3 }, input1);
	}

### TEST CODE
```
public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
     int temp = arr[arr.length - i - 1];
     arr[arr.length - i - 1] = arr[i];
     arr[i] = temp;
    }
  }
```





