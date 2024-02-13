# Lab Report 3
## Part 1 Bugs

***Failure-inducing input for the buggy program as a JUnit Test:***
The input that caused the failure was an array of ```{1,2,3,4} ```.
```
@Test
public void testReversed() {
    int[] input1 = new int[]{1,2,3,4,5};
    assertArrayEquals(new int[]{4,3,2,1},ArrayExamples.reversed(input1));
}
```

***Input that doesn't induce a failure as a JUnit test:***
The input that didnt cause a failure was an input of an empty array ```{} ```.
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

***Symptom (output) of the Failure-inducing input for the buggy program as a JUnit Test:***
The symptom of the failure inducing input was that at element 0 the value was 0 but was expected to be 5.

![Image](Screenshot 2024-02-12 124153.png)


***Symptom (output) of the Input that doesn't induce a failure as a JUnit test:***
The symptom of the input that doesn't induce a failure is that all tests passed. 

![Image](Screenshot 2024-02-12 123937.png)

***Bug code before : Broken***

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
}
```

***Bug code after: Fixed***

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```

***Bug code fix explanation:***

The reason the original code did not work was because in the for loop when iterating over the original aray, we were assigning the old array the values from the new array which were all zeros. And then we return the old array. 

The new code fixes this because as we are iterating over the original array, we are assigning the new array the values of the old array then once the loop is done we are returning the correct newly coppied array. 


## Part 2 - Researching Commands

### Find command 

***Find command with -name examples: ```find -name <file/directory name>```***

source for where I found how to use this command ["https://adamtheautomator.com/bash-find/"]

Example 1
```
noaht@nyogaL MINGW64 ~/OneDrive/Documents/GitHub/docsearch (main)
$ find -name "biomed"
./technical/biomed
```
What is happening is when you use  ```find -name "biomed"``` is it searches for the directory named biomed and displays the path to it. This is useful because you can ue this command instead of using cd and ls to look for the directory you need. 

Example 2
```
noaht@nyogaL MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -name "water_fees.txt"
./government/Media/water_fees.txt
```
What is happending is that when I used ```find -name "water_fees.txt"``` is that it searches for the file named water_fees.txt and displays the path to the file. This is useful becasue you can just use this command instead of navigating through the files with ls and cd.

***Find command with > examples: ```find <directory name> > <file>.txt```***

Example 1

Input:
```
noaht@nyogaL MINGW64 ~/OneDrive/Documents/GitHub/docsearch (main)
$ find technical/ > find-results-test.txt
```
Output: the file find-results-test.txt was created and all of the directories 

Example 2
```

```


