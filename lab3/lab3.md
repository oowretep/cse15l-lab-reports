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
![Image](img/message1.png)

---------********-------


Below are two screenshots of using `/add-message`:
![Image](img/message1.png)
> The method used in my request is `handleRequest`. The relevant argument is the URL that is passed in and the relevant values are the chat history field of the class `String chat`, the arrays of strings `String[] params`, `String[] messageArr` and `String[] userArr`. The values of the string arrays get changed based on the URL that is passed in. In this case, the URL is now dealing with a query of the message `Hello` from `jpolitz`. The values of `params`, `messageArr` and `userArr` are now changed to hold the query values. Then the `chat` string is updated to include `jpolitz: Hello`

![Image](img/message2.png)
> The method used in my request is the same as above. The relevant arguments are still the same as the URL is being passed in and the relevant values of `chat`, `params`, `messageArr` and `userArr` are still being used. In this case, the URL is now dealing with a query of the message `How are you` from `yash`. The values of `params`, `messageArr` and `userArr` are now changed to hold the query values. The `chat` string previously held `jpolitz: Hello` and the chat line `yash: How are you` is concatenated onto it (with `\n\n` for two newlines to provide some spacing).

---

## Part 2
Private Key path: /Users/peter/.ssh/id_rsa
![Image](img/privatekey.png)

Public Key path:/home/linux/ieng6/oce/42/442/pjwoo/.ssh/authorized_keys
![Image](img/publickey.png)

Logging into `ieng6` without being prompted for password:
![Image](img/loginnopass.png)

---

## Part 3
- From week 2, I learned how to create a Java Server. It was interesting to look at the base code for `Server.java` and see how the server functions and what is needed to create one. I also learned how to remotely connect to `ieng6` and how to setup a remote server using the connection. It was really cool to see the number incrementer app work on different devices, locally and remotely, and see it update.
- From week 3, I learned how to setup an SSH key to login wihout being asked for a password. When setting up the SSH key, I learned about `scp` and what the command does. I also learned how to use `man` to look up command manuals in the terminal without having to search it up online.

*note: added the private and public key paths to part 2 for regrade request.
