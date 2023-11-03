# LAB REPORT 3 #

## Symptoms and Failure- Inducing Inputs using Array Methods ##

The bug I am choosin for this lab report is the `reversedInPlace` bug.

### The failure inducing input

``` public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 2, 3, 6  };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{6 ,3 ,2 }, input1);
	}
```
