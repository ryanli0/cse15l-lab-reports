# Lab Report 3
### Provide:

### A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
```bash
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
```bash
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
### Briefly describe why the fix addresses the issue.
