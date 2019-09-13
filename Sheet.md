# CIS 200 Syntax Guide

## Table of Contents
[Foreword](#Foreword)<br/>
[Printing](#Printing)<br/>
[Initializing and Using Variables](#Initializing-and-Using-Variables)<br/>
[Reading in User Input](#Reading-in-User-Input)<br/>
[Formatting Numbers with Decimals](#Formatting-Numbers-with-Decimals)<br/>
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
    Scanner s = new Scanner(System.in);
    
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
    DecimalFormat df = new DecimalFormat("#0.00");
    
    double pi = 3.141592;
    System.out.println(df.format(pi));
    //Outputs -> 3.14
  }
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
```

## Arrays
I find it helpful to think of arrays as tables with pre-defined lengths. The following table demonstrates what you might imagine an array to look like that is of length 10 and has all zeros.<br/>

| Index:        | 0           | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:|
| Value:      | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

## Functions
WORK IN PROGRESS
