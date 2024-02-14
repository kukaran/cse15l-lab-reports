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
