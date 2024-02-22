# Lab 4

## Log into `ieng6`
![Image](img/1.png)
> Use `ssh [username]@ieng6.ucsd.edu` to login to `ieng6`

![Image](img/2.png)

## Clone the repo
![Image](img/3.png)
> Use `git clone [repo name]` to clone the repo that we forked

![Image](img/4.png)

## Run the test
![Image](img/5.png)
> First we are going to `ls` to see the files in the repo we cloned. Then using the `cd` command, we will move into the `lab7` directory. Then using `ls` again, we can see the `test.sh` script that we can run.

![Image](img/6.png)
> Running the test using `bash test.sh`, we can see that a test has failed

## Fixing the code
![Image](img/7.png)
> To fix the code, we will use `vim ListExamples.java` to fix the error

![Image](img/8.png)
> Here, we have `ListExamples.java` opened and we are at the beginning of the file. We know that the error is at the end of the file, so we can use `<ctrl>+g` to move to the end. Then use `<shift>+g` to move to the end. Then we will use `<h>` 6 times to move to the line that has the error. Then use `<e>` to move to the end of the word (specifically `index1`) and then `<r><2>` to replace the `1` with a `2`.

![Image](img/9.png)
> Now that the line is fixed, we can use `:wq` to save and quit

![Image](img/10.png)
![Image](img/11.png)
![Image](img/12.png)
![Image](img/13.png)
![Image](img/14.png)
![Image](img/15.png)
![Image](img/16.png)
![Image](img/17.png)
