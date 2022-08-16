# Java

This is a summary of Java syntaxis.

## Índice

1. [Print](#print)
1. [Variables](#variables)
1. [Comments](#comments)
1. [Input](#input)
1. [Primitive operators](#primitive-operators)
1. [Increment operators](#increment-operators)
1. [String concatenation](#string-concatenation)
1. [Conditionals](#conditional-statements)
   - [Comparison operators](#comparison-operators)
   - [Logical operators](#logical-operators)
   - [if / else if / else](#if-else-if-else)
   - [switch case](#switch-case)
     - [switch expression](#switch-expression)
1. [Loops](#loops)
   - [While](#while-loops)
   - [For](#for-loops)
   - [Do While](#do-while)
   - [Continue and Break](#continue-and-break)
1. [Arrays](#arrays)
   - [Creating arrays](#creating-arrays)
   - [Initialize arrays](#initialize-arrays)
1. [Array operations](#array-operations)
   - [Length](#length)
1. [Enhanced for loop](#enhanced-for-loop)
1. [Multidimensional arrays](#multidimensional-arrays)
1. []()
1. []()
1. []()
1. []()

## Print

[Índice](#índice)

To send a line to the console:

```java
System.out.println("Hello world");

```

## Data types

[Índice](#índice)

The most common data types that exists in Java are

- int
- double / float / long
- String
- char
- boolean
- void (just in methods)

## Variables

[Índice](#índice)

To declare a variable you must follow the following structure:

| visibility | data type | name | ;   |
| ---------- | --------- | ---- | --- |

You can either just declare the variable or you can also asign the value.

```Java
String name;
name = "Hi";

// or

int age = 18;
```

## Comments

[Índice](#índice)

There are two ways of making comments in Java. The single line comment and the block or multi-line comment.

```Java
// single line comment

/*
multi-line
comments
*/
```

## Input

[Índice](#índice)

To get user input you use the Scanner class.

```Java

// 1. import the class
import java.util.Scanner;

class MyClass {
  public static void main(String[ ] args) {

    // 2. create an instance of the class
    Scanner myVar = new Scanner(System.in);

    // 3. type the question
    System.out.println("Type your input")

    // 4. you can save it to a variable
    vari = myVar.nextLine();

    // 5. print
    System.out.println(vari);
  }
}

```

You can read different kinds of inputs the user enters

- Read a byte - **nextByte()**
- Read a short - **nextShort()**
- Read an int - **nextInt()**
- Read a long - **nextLong()**
- Read a float - **nextFloat()**
- Read a double - **nextDouble()**
- Read a boolean - **nextBoolean()**
- Read a complete line - **nextLine()**
- Read a word - **next()**

## Primitive operators

[Índice](#índice)

**\+** addition
**\-** subtraction
**\*** multiplication
**/** division
**%** modulo

## Increment operators

[Índice](#índice)

- **Increment operator**
  Increase the value of a variable by one

  ```Java
  int x = 1;
  // is equivalent to x = x + 1
  ++x; // x is now 2
  ```

- **Decrement operator**
  Decrease the value of a variable by one

  ```Java
  int x = 2;
  --x; // x is now 1
  ```

- **Addition and assingment**
  ```Java
  int a = 5;
  int b = 6;
  // equivalent a = a + b
  a += b; // a is 11 and b is 6
  ```
- **Substraction and assingment**
  ```Java
  int a = 5;
  int b = 6;
  // equivalent a = a - b
  a -= b; // a is -1 and b is 6
  ```
- **Multiplication and assingment**
  ```Java
  int a = 5;
  int b = 6;
  // equivalent a = a * b
  a *= b; // a is 30 and b is 6
  ```
- **Division and assingment**
  ```Java
  int a = 18;
  int b = 6;
  // equivalent a = a / b
  a /= b; // a is 3 and b is 6
  ```
- **Remainder and assingment**
  ```Java
  int a = 14;
  int b = 6;
  // equivalent a = a % b
  a %= b; // a is 2 and b is 6
  ```

There are tow forms of using the increment operators, _prefix_ and _postfix_.

**Prefix**: operation first and uses the new value in the expression.

```Java
int x = 3;
int y = ++x; // y is 4 and x is 4
```

**Postfix**: variable's value first used in the expression and is then realized the operation.

```Java
int x = 3;
int y = x++; // y is 3 and x is 4
```

## String concatenation

[Índice](#índice)

```Java
String a, b;
a = "Hola";
b = "Mundo";
System.out.println(a + " " + b) // Hola Mundo
```

## Conditional statements

### Comparison operators

[Índice](#índice)

- **<** less than
- **\>** greater than
- **!=** not equal to
- **==** equal to
- **<=** less than or equal to
- **\>=** greater than or equal to

### Logical operators

[Índice](#índice)

- **&** and
- **&&** and
- **|** or
- **||** or
- **!** not

The double operator (&& / ||) do not necessarily compares both conditions. Taking the truth tables of each operator it can skip a comparisson.

If you use a || and the first condition is true, it does not make the second comparison because it will be **`true`**.

If you use && and the first condition is false, it does not make the second comparison because it will be **`false`**.

### if else if else

[Índice](#índice)

```Java
if (condition) {
    //...
} else if (condition) {
    // ...
} else {
    // ...
}
```

### switch case

[Índice](#índice)

The break statement helps to end the switch, and jump to the next line after the switch. The break could not be necesary, so when the case ends it compares the next cases.

```Java
switch (expression) {
    case value1: {

        // ...
        break; // optional
    }
    case value2: {

        // ...
        break;
    }
    default: {// optional
        // ...
    }
}
```

```Java
int day = 1;

switch(day) {
  case 1:
    ++day;
    System.out.println("Monday");
  case 2:
    System.out.println("Tuesday");
    break;
  case 3:
    System.out.println("Tuesday");
    break;
  default:
    System.out.println("Not a valid day");
}
// Monday Tuesday
```

#### switch Expression

[Índice](#índice)

**->** shorthand

```Java
int day = 2;

String dayType  = switch(day) {
    case 1, 2, 3, 4, 5 -> "Working day";
    case 6, 7 -> "Weekend";
    default -> "Invalid day";
};

System.out.println(dayType);
```

## Loops

### While loops

[Índice](#índice)

```Java
while (condicion) {
    // ...
}
```

```Java
int x = 3;

while (x > 0) {
    System.out.println(x);
    x--;
}
```

### For loops

[Índice](#índice)

```Java
for (initialization; condition; increment/decrement) {
    // ...
}
```

```Java
for (int x = 1; x <=5; x++) {
    System.out.println(x);
}
```

### Do While

[Índice](#índice)

Similar al while normal, con la diferencia de que se ejecuta al menos una vez.

```Java
int x = 1;

do {
  System.out.println(x);
  x++;
} while(x < 0);

// 1
// the condiction is not true, however it is executed once
```

### Continue and Break

[Índice](#índice)

**break:** ends the loop and skips all the code inside the loop. _End the loop here_.

**continue:** skip the reamainder code inside the loop, and retest the condition to reiterate. _Go to next iteration_.

## Arrays

[Índice](#índice)

### Creating arrays

[Índice](#índice)

The arrays must have just one data type in all the positions.

Declaring an array.

```Java
int[] arr;
// or
int arr[];
```

Define array's capacity.

```Java
int[] arr = new int[5];
```

The arrays are zero-indexed. Asign values.

```Java
arr[2] = 42;

for (int x = 0; x < 5; x++) {
  System.out.println(arr[x]);
}

// 0 0 42 0 0
```

### Initialize arrays.

[Índice](#índice)

If you already know what values to insert in the array, you can use an array literal. Place the values in a comma-separated list, enclosed in curly braces.

```Java
String[] myNames = {"A", "B", "C", "D"};
System.out.println(myNames[2]); // C

int[] myNums = {1, 2, 3, 4};
System.out.println(myNums[2]); // 3
```

## Array operations

[Índice](#índice)

### Length

```Java
int[] intArr = new int[5];
System.out.println(intArr.length);
```

## Enhanced for loop

[Índice](#índice)

Is used to traverse elements in arrays.

```Java
int[] primes = {2, 3, 5, 7};

// It is readed as
// for t in primes
for (int t: primes) {
  System.out.println(t);
}

// 2 3 5 7
```

## Multidimensional Arrays

[Índice](#índice)

Arrays can contain other arrays.

```Java
int[][] sample = {{1, 2, 3}, {4, 5, 6}};

int x = sample[1][0];
System.out.println(x); // 4
```

##

[Índice](#índice)

##

[Índice](#índice)

##

[Índice](#índice)

##

[Índice](#índice)
