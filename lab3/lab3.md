# Lab 3

## Part 1
The bug I chose was the ArrayExamples
- A failure-inducing input for the buggy program, as a JUnit test and any associated code:

Test:
```
@Test 
public void testReverseInPlace2() {
  int[] input1 = { 1, 2, 3, 4 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 4, 3, 2, 1 }, input1);
}
```
Associated Code: 
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

- An input that doesn't induce a failure, as a JUnit test and any associated code:

Test:
```
@Test 
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[] { 3 }, input1);
}
```
Associated Code: 
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

- The symptom, as the output of running the tests:
![Image](img/symptomImg.png)


- The bug, as the before-and-after code change required to fix it:

Before:
```
static void reverseInPlace(int[] arr) {
  for (int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```
After:
```
static void reverseInPlace(int[] arr) {  
  for (int i = 0; i < arr.length / 2; i++) {
    int temp = arr[i];
    arr[i] = arr[arr.length - 1 - i];
    arr[arr.length - 1 - i] = temp;
  }
}
```

This code was buggy because it was not storing the values when swapping them without using any sort of temp storage. Adding a temp int, I was able to fix the bug and reverse the array in place without needing a temp array.

---

## Part 2
I chose to look into the `grep` command

1. Recursive search with `-r` (ChatGPT source):
```
