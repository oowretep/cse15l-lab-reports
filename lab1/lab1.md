# Lab 1

## Using `cd`
When using the `cd` command with no arguments, we can see the following output:

![Image](images/cd%20no%20arg.png) 

> When the working directory was the root (`~`) directory, we can see no change happening and we remain in the root directory.
When we `cd` into another directory like `lecture1`, we can see that using the `cd` command with no arguments brings us back to the root directory.
> There was no error when running `cd` with no arguments.

When using the `cd` command with a path to a directory as an argument, we can see the following output:

![Image](lab1/images/cd%20dir.png) 

> The working directory was the root (`~`) directory and using the command `cd lecture1` brought us into the `lecture1` direcory
> There was no error when running `cd` with a directory as an argument.

When using the `cd` command with a path to a file as an argument, we can see the following output:

![Image](lab1/images/cd%20file.png) 

> The working directory was the lecture1 (`~/lecture1`) directory and using the command `cd Hello.java` gave us an output of `bash: cd: Hello.java: Not a directory`
> This output was an error since we can not `cd` into a file.

---

## Using `ls`
When using the `ls` command with no arguments, we can see the following output:

![Image](lab1/images/ls%20no%20arg.png)

> The working directory was the root (`~`) directory, and we see an output of `lecture1` since that is the only item within the root directory. 
> There was no error when running `ls` with no arguments.

When using the `ls` command with a path to a directory as an argument, we can see the following output:

![Image](lab1/images/ls%20dir.png) 

> The working directory was the root (`~`) directory and using the command `ls lecture1` gave us an output of all the items within the `lecture1` directory.
> There was no error when running `cd` with a directory as an argument.

When using the `ls` command with a path to a file as an argument, we can see the following output:

![Image](lab1/images/ls%20file.png) 

> The working directory was the lecture1 (`~/lecture1`) directory and using the command `ls Hello.java` gave us an output the item itself since it is a single file.
> There was no error when running `ls` with a directory as an argument.

---

## Using `cat`
When using the `cat` command with no arguments, we can see the following output:

![Image](lab1/images/cat%20no%20arg.png)

> The working directory was the root (`~`) directory, and we see that the command is running indefinitely as pressing `enter` or any other key will result in those being listed out as seen in the screenshot. The command will continue to run, resulting in the terminal being "stuck", until `ctrl-c` (for mac) is used to exit the command. 
> This output can be considered an error when using the `cat` command with no arguments since the desired output is not what we want. The `cat` argument expects a file name so it will continue to "stall" until a file name is passed in or else we need to exit the command.

When using the `cat` command with a path to a directory as an argument, we can see the following output:

![Image](lab1/images/cat%20dir.png) 

> The working directory was the lecture1 (`~/lecture1`) directory and using the command `cat messages/` gave us an output of `cat: messages/: Is a directory`
> This output is an error since the `cat` command expects a file and not a directory as its argument.

When using the `ls` command with a path to a file as an argument, we can see the following output:

![Image](lab1/images/cat%20file.png) 

> The working directory was the lecture1 (`~/lecture1`) directory and using the command `cat Hello.java` gave us an output of the contents of the `Hello.java` file as seen in the screenshot above.
> There was no error when running `cat` with a file as an argument.
