Lerea Data Structures 101
Homework 1
Grade Storage System

Before we get started with this assignment, like all good assignments you will learn something new! In our first session we talked about how to produce output, or print, in programs. Printing is done in one of two ways:

1. `System.out.print(<item you want printed>)`

2. `System.out.println(<item you want printed>)`

As we talked about the only difference between the two functions shown about is that the latter prints a newline after the item printed. This will result in the next item printed being on a separate line.

Now, let’s talk about how to take in input into a program. Without input, programs are boring. You need the user of your program to have the ability to input information that your program can then process or store.

In JAVA we use a Scanner to read input and store that input into variables. Scanners are types that read input in very easy ways. Here’s an example:

Scanner keyboardInput = new Scanner(System.in);

String firstWord = keyboardInput.next();
String secondWord = keyboardInput.next();

Each subsequent call to the function next() will return the next ‘token’ or word of input. The Scanner will return that input as a String. Note that if your program calls the next() function it will wait until the user puts in input into the program. This means that the program can prompt the user for some input and then wait until it is given before acting on it, for example:


Scanner kb = new Scanner(System.in);
System.out.println(“Please input your first name: “);
String firstName = kb.next();
System.out.println(“Please input your last name: “);
String lastName = kb.next();

System.out.println(“Your full name is: “ + firstName + “ “ + lastName);

One last thing and then we will move on to the assignment: In order to use a Scanner in your program it must first be imported. This is done by writing the following line at the top of the file:

“import java.util.Scanner”. We will go into more detail later into what that means.



I hope that lesson was informative because it will be needed to complete this first assignment! 


