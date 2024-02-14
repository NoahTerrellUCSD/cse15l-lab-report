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

source for where I found how to use this command [https://adamtheautomator.com/bash-find/](https://adamtheautomator.com/bash-find/)

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

***Find command with -type examples: ```find <name> -type <type>```***

source for where I found how to use this command [https://www.redhat.com/sysadmin/linux-find-command](https://www.redhat.com/sysadmin/linux-find-command)

Example 1

```
noaht@nyogaL MINGW64 ~/OneDrive/Documents/GitHub/docsearch (main)
$ find technical -type d
technical
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```
What is happening is that when you use the find command with a directory and then add the -type command with d following it like this ```find technical -type d``` is that you are basically saying to find inside the technical directory any thing that is type directory. As you can see when we did this it returns every directory inside of the technical directry. This is helpful because we may want to look at all of the directories in a specific directory. 

Example 2
```
noaht@nyogaL MINGW64 ~/OneDrive/Documents/GitHub/docsearch (main)
$ find technical/plos -type f
technical/plos/journal.pbio.0020001.txt
technical/plos/journal.pbio.0020010.txt
technical/plos/journal.pbio.0020012.txt
technical/plos/journal.pbio.0020013.txt
...

```
What is happening is that when you use find with a path and then the command -type with f following it like this ```find technical/plos -type f``` is that you are basically saying to find in this path anything of the type file so basically all of the files. As you can see when we do this it returns all of the files in the technical/plos path. This is usefull because you may be looking for only files inside of a path and you may not want to see any directories and only the files inside that path. 


***Find command with -maxdepth and -type examples: ```find <path> -maxdepth <number> -type <type>```***

source for where I found how to use this command [https://www.redhat.com/sysadmin/linux-find-command](https://www.redhat.com/sysadmin/linux-find-command)

Example 1
```
$ find technical/ -maxdepth 1 -type d
technical/
technical/911report
technical/biomed
technical/government
technical/plos

```
What is happening is that when I use find with a path with the -maxdepth command with a number parameter and the -type d command like this ```find technical/ -maxdepth 1 -type d``` is that im basically saying to find all of the directories one directory deep inside of the path which is why the terminal returned only the paths that are one directory after the one that I chose. This is helpful because if there are a bunch of nested directories in a directory then you can use this to see only the first layer but if you wanted to go deeper than you could jut change the number after the -maxdepth command. 

Example 2
```
noaht@nyogaL MINGW64 ~/OneDrive/Documents/GitHub/docsearch (main)
$ find technical/government/ -maxdepth 2 -type f
technical/government/About_LSC/Comments_on_semiannual.txt
technical/government/About_LSC/commission_report.txt
technical/government/About_LSC/conference_highlights.txt
technical/government/About_LSC/CONFIG_STANDARDS.txt
technical/government/About_LSC/diversity_priorities.txt
technical/government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
technical/government/About_LSC/Progress_report.txt
technical/government/About_LSC/Protocol_Regarding_Access.txt
...
```
What is happening is that when I use the find command with a path and then use the -maxdepth command with a parameter and the -type f command like this ```find technical/government/ -maxdepth 2 -type f``` is that im basically saying to find all of the files 2 directories deep in the government drectory which is why the terminal returned a bunch of files. This is useful because if I wanted to look at all of the files two directories deep in the government directory then I can just use this. 





3: 
$ find technical/ -maxdepth 3 -type d -or -type f

