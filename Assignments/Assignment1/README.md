# Assignment 1 - Grade Storage System

## Table of Contents
1. [Background](#background)
2. [Assignment](#assignment)
    1. [Input a new grade](#input-a-new-grade)
    2. [Change an existing grade](#change-an-existing-grade)
    3. [View an existing grade](#view-an-existing-grade)
    4. [Exit](#exit)
3. [Examples](#examples)
    1. [Simple input and view](#simple-enter-and-view-a-grade)
    2. [Try to add invalid grade](#try-to-add-invalid-grade)

## Background

Before we get started with this assignment, like all good assignments you will learn something new! In our first session we talked about how to produce output, or print, in programs. Printing is done in one of two ways:

```java
System.out.print(<item you want printed>);

System.out.println(<item you want printed>);
```

As we talked about, the only difference between the two functions shown above is that the latter prints a newline after the item printed. This will result in the next item printed being on a separate line.

Now, let’s talk about how to take in input into a program. Without input, programs are boring. You need the user of your program to have the ability to input information that your program can then process or store.

In JAVA we use a Scanner to read input and store that input into variables. Scanners are types that read input in very easy ways. Here’s an example:

```java
Scanner keyboardInput = new Scanner(System.in);

String firstWord = keyboardInput.next();
String secondWord = keyboardInput.next();
```

Each subsequent call to the function next() will return the next ‘token’ or word of input. The Scanner will return that input as a String. Note that if your program calls the next() function it will wait until the user puts in input into the program. This means that the program can prompt the user for some input and then wait until it is given before acting on it, for example:

```java
Scanner kb = new Scanner(System.in);
System.out.println(“Please input your full name: “);
String firstName = kb.next();
String lastName = kb.next();

System.out.println(“Your full name is: “ + firstName + “ “ + lastName);
```

Scanners can also be used to read in integers. This can be done as follows:

```java
Scanner kb = new Scanner(System.in);
System.out.println("Please enter a number to multiply by 2");
int number = kb.nextInt();
System.out.println(number * 2);
```

**One last thing** and then we will move on to the assignment: In order to use a Scanner in your program it must first be imported. This is done by writing the following line at the top of the file:

```java
import java.util.Scanner;
```
We will go into more detail later into what that means.

## Assignment

I hope that lesson was informative because it will be needed to complete this first assignment! For this first excursion into the wonderful world of JAVA we will build a grades storage and retrieval system. This system will enable its user to input all students in a given class, input their grades, and change their grades as needed.

First the user should be prompted with a question:
```
Welcome to the grade storage system.
What is the maximum number of students in the class?
```
Once this question is answered the user will be brought to the main menu:
```
What would you like to do?
1. Input a new grade
2. Change an existing grade
3. View an existing grade
4. Exit
```

Now, lets tackle each one of these options one at a time:

### Input a new grade

If the user chooses this option they should be prompted for the student's name and grade as follows:
```
What is the students name and grade?
```

The input format should be the following:
```
<firstname> <lastname> <letter grade>
```

The following grades are legal:
1. A
2. B
3. C
4. D
5. F

If the user inputs an invalid grade they should be met with the following error message before returning to the main prompt:
```
Invalid grade, please try again.
```

If the user inputs a name that has already been entered they should be met with the following error message before returning to the main prompt:
```
This student already has a grade, please try again.
```

If there are already the maximum number of students entered the user should be met with the following error message:
```
There are too many students! Please no longer use option 1.
```

Otherwise the program should output the following success message and then return to the original menu.
```
Grade added
```

### Change an existing grade

If the user chooses this option they should be prompted for the user's name and new grade as follows:
```
What is the students name and new grade?
```

The input format will be the following:
```
<firstname> <lastname> <new letter grade>
```

As with inputting a new grade, if the letter grade provided is invalid the user should be met with the same error message as above. If the student entered does not yet have a grade the user should be met with the following error:
```
This student does not yet have a grade, please use option 1 to enter a new grade.
```

Otherwise the program should output the following success message and then return to the original menu.
```
Grade Changed
```

### View an existing grade

If the user chooses this option they should be prompted for the students name as follows:
```
What is the students name?
```

The input format will be the following:
```
<first name> <last name>
```

If the name provided does not yet have a grade the user should be met with the following error message:
```
This student does not yet have a grade, please use option 1 to enter a new grade.
```

If the student already has a grade the program should print that students grade as entered using option 1 or updated using option 2 and then return to the main menu.

### Exit

If the user chooses this option the program should stop.

## Examples

### Simple enter and view a grade
```
Welcome to the grade storage system.
What is the maximum number of students in the class?
```
`10`
```
What would you like to do?
1. Input a new grade
2. Change an existing grade
3. View an existing grade
4. Exit
```
`1`
```
What is the students name and grade?
```
`Tuvia Lerea A`
```
Grade added
What would you like to do?
1. Input a new grade
2. Change an existing grade
3. View an existing grade
4. Exit
```
`3`
```
What is the students name?
```
`Tuvia Lerea`
```
A
What would you like to do?
1. Input a new grade
2. Change an existing grade
3. View an existing grade
4. Exit
```
`4`

### Try to add invalid grade
```
Welcome to the grade storage system.
What is the maximum number of students in the class?
```
`10`
```
What would you like to do?
1. Input a new grade
2. Change an existing grade
3. View an existing grade
4. Exit
```
`1`
```
What is the students name and grade?
```
`Tuvia Lerea E`
```
Invalid grade, please try again.
What would you like to do?
1. Input a new grade
2. Change an existing grade
3. View an existing grade
4. Exit
```
