# Lab Report 3
### Provide:

### A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
```java
public class ArrayTests {
    @Test
  public void testReverseInPlace() {
      int[] input = {1, 2, 3, 4};
      ArrayExamples.reverseInPlace(input);
      assertArrayEquals(new int[]{4, 3, 2, 1}, input);
  }
}
```
### An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
```java
public class ArrayTests {
    @Test
  public void testReverseInPlace() {
      int[] input = {3};
      ArrayExamples.reverseInPlace(input);
      assertArrayEquals(new int[]{3}, input);
  }
}
```
### The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
![Image](Lab3Step3.png)
### The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
##### reverse method Before:
```java
 // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
##### reverse method After:
```java
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        newArray[i] = arr[arr.length - i - 1];
    }
    for(int i = 0; i < arr.length; i++){
        arr[i] = newArray[i];
    }
  }
```
### Briefly describe why the fix addresses the issue.
##### Before fixing the issue, the method would parse over the array, replacing the first elements before being able to move the first elements to the end. This is not the intended effect since it would effectively result in an array that is only partially reversed. {1, 2, 3, 4} would end up looking like {4, 3, 3, 4} since the last two elements are reversed in reference to the beginning of the array. In order to fix this, a temporary array is created to move each item to a fresh "workspace", thus allowing the overwriting problem to be resolved.
