# CIS 200 Syntax Guide

## Table of Contents
[Foreword](#Foreword)<br/>
[Printing](#Printing)<br/>
[Initializing and Using Variables](#Initializing-and-Using-Variables)<br/>
[Reading in User Input](#Reading-in-User-Input)<br/>
[Formatting Numbers with Decimals](#Formatting-Numbers-with-Decimals)<br/>
[If Statements](#If-Statements)<br/>
[Loops](#Loops)<br/>
[Arrays](#Arrays)<br/>
[Functions](#Functions)<br/>

## Foreword
This is not supposed to be a replacement for lectures or Java textbooks. With that being said, this should be a helpful supplemental material. 

## Printing
```java
//println brings the cursor to the next line
System.out.println("Hello");
System.out.println("World");
//Outputs ->
//Hello
//World

//print leaves the cursor on the same line
System.out.print("Hello ");//Notice the space after Hello
System.out.print("World");
//Outputs ->
//Hello World

//print a variable along with text
int x = 5;
System.out.println("X is equal to " + x);
//Outputs ->
//X is equal to 5
```

## Initializing and Using Variables
* Each variable **MUST** have a unique name
* Each variable must be assigned a type (int, char, etc..)
```java
int x = 5;//Integers do not have decimal places
double y = 5.0;//doubles have decimal places
String str = "Test 5";//Strings are surrounded by double quotes
char c = 'y';//Chars are surrounded by single quotes

```

## Reading in User Input
To read user input we must import the scanner
```java
import java.util.*;//This line imports the scanner. Also this must be placed above the class
public class Test 
{
  public static void main(String[] args) 
  {
    Scanner s = new Scanner(System.in);//Create the scanner object
    
    String str = s.nextLine();
    char c = s.nextLine().charAt(0);//Get first character of the user inputted string
    int x = Integer.parseInt(s.nextLine());//Do not use "s.nextInt()"! Always use Integer.parseInt(s.nextLine())
  }
}
```

## Formatting Numbers with Decimals
```java
import java.text.*;//This line imports the DecimalFormat. Also this must be placed above the class
public class Test 
{
  public static void main(String[] args) 
  {
    DecimalFormat df = new DecimalFormat("#0.00");//Create the DecimalFormat object
    
    double pi = 3.141592;
    System.out.println(df.format(pi));
    //Outputs -> 3.14
  }
}
```

## If Statements
There are three variations of if statements: if, if else, and else
### If
```java
int x = 1;
if(x == 1)
{
  //The condition is met so this if will run
}
```

### Else if
Else if statements will not be run if one of the if statements it is linked to has its condition met.
```java
int x = 1;
if(x == 1)
{
  //Condition is met
}
else if (x > 1)
{
  //Will not run because an if statement before it ran
}
else if(x < 1)
{
  //Will not run because an if statement before it ran
}
```
### Else
Else statements are the cases that run when none of the if or else if conditions are met.
```java
int x = 5;
if(x == 1)
{

}
else if(x == 2)
{

}
else //Else statements do not need conditions: they rely on other if statements coming before them
{
  //Because x does not meet any of the preciding if conditionals, this else statement will run
}
```

## Loops
There are three main types of loops: for, while, and do while:
### For Loops
This is the loop that you will use the most. They are helpful for iterating over arrays.
```java
//General form
for([variable creation]; [variable condition]; [variable incrementation/decrementation])
{
}

//Example
for(int i = 0; i < 10; i++)
{
  //iterates from 0 to 9
}
```
### While Loops
Similar to do while loops, however, they will not run if the condition is not met.
```java
//Example
int i = 0;
while(i < 10)
{
  i++;
  //iterates from 0 to 9
}

int j = 11;
while(j < 10)//will not run because condition is not met
{
  j++;
}
//The value of j after the loop is still 11
```
### Do While Loops
Similar to while loops, however, they are guaranteed to run at least once even if the condition is not met.
```java
//Example
int i = 0;
do
{
  i++;
  //iterates from 0 to 9
}while(i < 10);

//This will run once and then terminate because the condition is not met
int j = 11;
do
{
  j++;
}while(j < 10);
//The value of j after the loop is 12 because it runs once before being terminated
```

## Arrays
I find it helpful to think of arrays as tables with pre-defined lengths. The following table demonstrates what you might imagine an array to look like that is of length 10 and has all zeros. Arrays are zero indexed, so the first position in the array is index 0<br/>

| Index:        | 0           | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:|
| Value:      | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
### Initializing Arrays
This creates an integer array of length 10. This would create the array you see represented in the table above.
```java
int[] thisIsAnIntArray = new int[10];
```
### Accessing/Setting Values in Arrays
Now that we have created an array we can set or access its values. **DO NOT** access a position that is outside the bounds (length) of the array: doing so will crash your program.
```java
int[] thisIsAnIntArray = new int[10];

thisIsAnIntArray[0] = 3;//Set the value of index 0 to 3
thisIsAnIntArray[5] = 7;//Set the value of index 5 to 7
```
The above code would change the values at positions 0 and 5 to the given values. This is represented below.<br/>

| Index:        | 0           | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:|
| Value:      | 3 | 0 | 0 | 0 | 0 | 7 | 0 | 0 | 0 | 0 |
```java
int[] thisIsAnIntArray = new int[10];

thisIsAnIntArray[0] = 3;
thisIsAnIntArray[5] = 7;
System.out.println("The value of index 5 in the array is: " + thisIsAnIntArray[5]);//Access the value of index 5
//Outputs -> 
//The value of index 5 in the array is: 7
```
## Functions
WORK IN PROGRESS
