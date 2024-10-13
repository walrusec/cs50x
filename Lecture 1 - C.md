# Lecture 1 - C
## Header Files
Header files are the libraries that we use with the C language. We use the format below to use a C header
```c
#include <stdio.h>
```

***
## Variables
We are required to specify our type when setting a variable
```c
string answer = function();
```

```c
# declare a variable
int counter = 0;
# increment the variable
counter = counter + 1;
counter += 1;
counter++;
counter--; 
```

***
## Printing Data
We use the #printf function to print data, and we use `%s` as a placeholder for substituting strings
```c
printf("hello, %s\n", answer);
```

Other substitution codes are:
```plaintext
%c - conditionals
%f - floats
%i - integers
%li - 
%s - strings
```

lil-program.c
```c
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	string answer = get_string("whats your name?");
	printf("Hello, %s\n", answer);
}
```

***
## Conditionals
we use if statements with parenthesis
```c
if (x < y) {
	printf("X is less than Y\n");
}
else if (x > y) {
	printf("X is greater than Y\n);
}
else {
	print("X is equal to Y"\n);
}
```

Why do we even use if/else?
multiple If's are inefficient, why ask new questions over and over, if we already know the answer?

We can use or/and conditions with || or &&
```c
if (c == 'y' || c == 'Y')
```

***
## Data types
### Char
Precisely one character. Good to use when you want confirmation when interacting with the user.
We should use single quotes when using a single character

We were familiar with other data types so they will not be defined.
***
## Loops
### While loops
we run forever; until some logic event occurs
```c
# we meow until our counter is <= 0
int counter = 3;
while (counter > 0)
{
	printf("not yet\n");
	counter = counter -1;
}
```

Convention however suggests we start at 0. ie:
```c
int counter = 0;
while (counter < 3)
{
	printf("not yet\n");
	counter++;
}
```

We can shorten it further with a #for-loop
```c
- [ ] for (int i = 0; i < 3; i++)
{
	printf("not yet\n");
}
```

to run a loop forever
```c
while (true)
{
	print("never\n");
}
```
***
## Functions
We use void when there is no return value for a function
```c
void nameOfFunction(void)
{
	printf("some phrase\n");
}
```

We need to make sure we define our functions before we reference them.
This does not mean that we should just shove them up top, so we define our functions below main, and we copy the #function-prototype `void nameOfFunction(void)` to the top, and define our function later

```c
#include <stdio.>

void nameOfFunction(void); # function prototype

int main(void)
{
  for (int i = 0; i < 3; i++)
	{
	  meow();
	}
}

void meow(void)
{
	printf("meow\n");
}
```

if we want to give our function an input, we give the prototype a type and a name, as well as the function
```c
#include <stdio.h>

void nameOfFunction(int n);

int main(void)
{
	meow(50);
}

void meow(int n)
{
  for (int i = 0; i < n; i++)
	{
	  printf("meow\n");
	}
}
```

When we want to return data we don't use void
We use int to specify what it should return
```c
#include cs50.h
#include stdio.h

int add(int a, int b)

int main(void)
{
	int x = get_int("x: ");
	int y = get_int("y: ");
	
	printf("%i\n", add(x + y));
}

int add(int a, int b)
{
	return a + b;
}
```

we always make main an #int, because our program returns a return code. 0, or an error code. 
***
## Constants