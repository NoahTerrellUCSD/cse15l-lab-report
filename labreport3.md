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

***Input that doesn't induce a failure as a JUnit test:***
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

***Symptom (output) of the Failure-inducing input for the buggy program as a JUnit Test:***
![Image](Screenshot 2024-02-12 124153.png)


***Symptom (output) of the Input that doesn't induce a failure as a JUnit test:***
![Image](Screenshot 2024-02-12 123937.png)



