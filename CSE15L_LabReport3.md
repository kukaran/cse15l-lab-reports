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
The left and right hand side of the `=` was switched in the line: `arr[i] = newArray[arr.length - i - 1];`. You want to reference the items in `newArray` from smallest to largest index to the items in `arr` from largest to smallest index. So simply switch `arr` and `newArray` in the line to `newArray[i] = arr[arr.length - i - 1];` Then return `newArray` instead of `arr` because in this method `newArray` is a new array that you are creating and modifiying based on the contents in `arr` which is the argument.

4 Ways to Use the `grep` command:

1. Using the `--color` option:

Example 1:
```
kumailkaran@Kumails-MacBook-Pro technical % grep --color "Bush" 911report/chapter-1.txt 
    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
    In Sarasota, Florida, the presidential motorcade was arriving at the Emma E. Booker Elementary School, where President Bush was to read to a class and talk about education. White House Chief of Staff Andrew Card told us he was standing with the President outside the classroom when Senior Advisor to the President Karl Rove first informed them that a small, twin-engine plane had crashed into the World Trade Center. The President's reaction was that the incident must have been caused by pilot error.
```
Screenshot:
![Image](GrepColorEx1.png)

Example 2:
```
kumailkaran@Kumails-MacBook-Pro technical % grep --color "crash" 911report/chapter-13.2.txt
                to indicate that the FAA recognized Flight 77 as a hijacking until it crashed into
                FBI found no evidence of a firearm at the crash site of Flight 93. See FBI response
                knives or portions of knives at the Flight 93 crash site. FBI report, "Knives Found
                1999, plane crash that killed Payne Stewart than it did to the hijacking of American
                and crash-site specific, and are based on time codes automatically recorded in the
                possibly from aircraft crash. Also, hijacking of American Flight 11 from Boston to
                addition to the two that had already crashed. Though the senior agent told someone
                time allowed for maneuvering or slowing to aim and crash the airplane into its
                operation of the airplane prior to its final maneuvers and crash, as well as for
```
Screenshot:
