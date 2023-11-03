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


  @Test
  public void testReversed() {
    int[] input1 = {3,4,5,6,7 };
    assertArrayEquals(new int[]{7,6,5,4,3}, ArrayExamples.reversed(input1));
  }
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

  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```


### The success inducing input

```
public class ArrayTests {
@Test 
public void testReverseInPlace() {
    int[] input1 = {1,2,3  };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3,2,1 }, input1);
	}
```


