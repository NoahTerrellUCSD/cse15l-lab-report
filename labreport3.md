# Lab Report 3
## Part 1 Bugs

***Failure-inducing input for the buggy program as a JUnit Test:***

```
@Test
public void testReversed() {
    int[] input1 = new int[]{1,2,3,4,5};
    assertArrayEquals(new int[]{4,3,2,1},ArrayExamples.reversed(input1));
  }
```

***Input that doesn't induce a failure, as a JUnit test:***
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
