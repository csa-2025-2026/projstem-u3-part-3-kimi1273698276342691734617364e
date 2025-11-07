[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=21534858)
# unit-3-assignment-3

## API and Documentation
Documentation for the shape classes can be found [here](https://coderunner.projectstem.org/docs/shapes/index.html).

## Git Config
```
git config user.name "user"
git config user.email "email"
```

## Compiling and Running Java Programs
Note that since the shape classes are separate classes, you will need to compile ALL the files (at least one time).  You can do this by running
```
javac *.java
```
The star means to compile every file that is a Java file type.

Run your code by running
```
java Main.java
```

After you compile the shape classes, you only need to compile and run `Main.java` as usual.

# Instructions  

## Problem 1
Write a program that takes in two integers as input, and displays `"Ratio OK"` if the ratio (or quotient) of the first input by the second input is between 1 exclusive and 8 inclusive.  If the user accidentally divides by 0, then display an error message instead.

## Problem 2
Write a program that takes in two integers, `a`, and `b`, as input and displays `"Is a factor"` if `b` is a factor of `a` (or in other words, if a is divisible by b).  If b is 0, then display an error message instead.

## Problem 3
Write a program that takes in an integer as input, and checks whether it is outside of the range 50-59 (inclusive). If it is outside of this range the program should print a warning and change the number to 55. 

Sample runs of the program functioning properly are below:

Sample run 1:
```
Enter a number in the fifties
51
Your number is 51
```
Sample run 2:
```
Enter a number in the fifties
33
That's not in the fifties!
Your number is 55
```

## Problem 4
Write a program that takes two inputs, x and y, from the user and print "pass" if one or more of the following is true:

- y is not greater than 9
- x is not less than or equal 2 and `x * y` is greater than 10
## Sample Solutions
```java
public class Main
{
	public static void main(String[] args)
	{
		Scanner sc = new Scanner(System.in);
		// Problem 1
		System.out.println("Enter two numbers:");
		int x = sc.nextInt();
		int y = sc.nextInt();

		if (y == 0)
		{
			System.out.println("Arithmetic exception");
		}
		else
		{
			double ratio = (double) x / y;
			if (1 < ratio && ratio <= 8)
			{
				System.out.println("Ratio OK");
			}
		}

		// Problem 2
		System.out.println("Enter two numbers:");
		int a = sc.nextInt();
		int b = sc.nextInt();

		if (b == 0)
		{
			System.out.println("Divide by 0 error");
		}
		else if (a % b == 0)
		{
			System.out.println("Is a factor");
		}

		// Problem 3
		System.out.println("enter a number in the fifties");
		int num = sc.nextInt();

		if (num < 50 || num > 59)
		{
			num = 55;
			System.out.println("That's not in the fifties");
		}

		System.out.println("Your number is " + num);

		// Problem
		System.out.println("Give two numbers");
		x = sc.nextInt();
		y = sc.nextInt();

		if (y <= 9 || x > 2 && x * y > 10)
		{
			System.out.println("pass");
		}
	}
}
```
