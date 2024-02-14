CSE15L Lab Report 3 
Kumail Karan 
PID: A17688437

Part 1 Bugs:

A failure-inducing input for the buggy program:
```
  @Test
  public void testReversed1() {
    int[] input1 = { 5,4,3,2,1 };
    assertArrayEquals(new int[]{ 1,2,3,4,5 }, ArrayExamples.reversed(input1));
  }
```
An input that doesn't induce a failure:
```
 @Test
  public void testReversed2() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
The symptom, as the output of running the tests:
![Image](SymptomFromRunningTests.png)

The bug, as the before-and-after code change required to fix it:

Before:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
Briefly describe why the fix addresses the issue:
The left and right hand side of the `=` was switched in the line: `arr[i] = newArray[arr.length - i - 1];`. You want to reference the items in `newArray` from smallest to largest index to the items in `arr`
