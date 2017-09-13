# 13.09.2017 #

## Farmer boys and girl in the IT ##

This topic sounds sarcastic, but it only address the issue that people
work as software developer that not called to be a software developer.
Then they are lacking on talents.

## Role of talent or giftings

## Fixing the wrong thing!!

Car diesel pump example 1400€ compared to a small pump.

## Start with business layer, know your business

.. not user interface layer
.. not backend layer / persistence layer

Software if often made in layers. Most used is a 3-layered-Architectur
to seperate User Interface, Business Logic and Data Persistance.

Some project start with an existing database and later build
a user interface and business layer on it. This can lead to unclean load.

Some start with the user interface and later make the business layer.

My experience over years you have to start with the business first.
You have to know you business. 

Some do not know their business and want to make an application.
If always use a house construction as metapher. If you do not
know that kind of house you want how could you implement it.
Some sit in meeting and says we want a house. Right a task
build a house and next they implementation starts. Someone
starts to build a house and when it is finished. Someone came
and look at and says this is not exactly what we want. But you
does not say how it should look. You only said build a house and
I build one. If you know what you not want. Do you know what
you want?

## Unclean factor

unclean information factor * unclean design factor * unclean impl factor * unclean 

50% * 70% * 80% = 28% (of 100%)

The early you catch better it is.

## Costs

IBM System Science Institute says to find a bug costs for instance in production 100
times more then in design phase.

Design 		  1x
Impl 		 10x
Testing 	 15x
Production 	100x

(see "The Ourageous Cost of Skipping TDD & Code Reviews" from Eric Elliot)

## Mission

String reduction of unclean software.

## iFixIt

iCleanUp for software is that was is iFixit for hardware

Repair your thinking phase (collecting information). 
Repair your design.
Repair your tests.
Repair your production code.

## Service

The service is to help people to fix their error
in any phase design, implementation, test, production.

The early you catch the better.

## Role of design

Good design lead to compact error free code. Non-spagetti.
Good design simplify.

## Change, Change, Change, ...

## Boss vs. Authority

Lack of good authority leads to bosses. (little mafia)

## Who is the boss

## Keep it complicated

A complicated thinker will always made out of simple or normal thing
a comlpicated thing.

(e.g. 16 pages DWGTiler vs. 4 Pages)

# Weed seed is growing

Unclean design spread out and product weed software.
Weed is growing with every feature you build in.

(e.g. 30 sensor, 50 reports)

A sign is if you inplement a feature and you have
to change it always n-times in the code.

If you have n different content types and you change
and you change it not on one position but have to change
it n-times.

# Simple Robust Good Programming #

## if (obj == null) ##
I do not like NullReference Exception. Why?

First a NullReferenceException is not an exception. If you create a variable that has not value. Is not an exception. Perhaps you have a variable that is empty. Not set. Not defined. The reason why you get a NullReferenceException is, you want access a property from an object that does not exists or is empty or undefined or not set. Whatever? It is more something like.

var a = string.Empty;  // This has a type string but is empty
var b = double.NaN;    // This has a type double and is NaN - Not a Number;
var c = undefined;     // This has not type - Empty what? NotDefined what? 

What means Null? Null means that the object does not exists or is empty or is not defined or whatever. You have yourself define what you mean with null. So why this is an exception? If you have fill out a form where you fill out your FirstName, LastName and you have not started to fill the form out, then the fields in the form are empty. And also the whole the form self is empty.

*Example 1:*

Let say we have Form with your Person data to fill out:

~~~
-------- FORM ----------------

FirstName: [________]
 
 LastName: [________]

 Birthday: [________]     

------------------------------
~~~

The class that stores the Data of the Form:

 ~~~
class Person
{
	string FirstName; // this should string.Empty
	string LastName;  // this should string.Empty, too
}
~~~
PROBLEM!! Person.Empty is static Reference to an Empty object.

~~~
var aPerson = Person.Empty;
aPerson.FirstName = "foo";
aPerson.LastName = "bar";
~~~

Sets the properties of this static object !!

~~~
var person = Person.Empty;
person.Age; // Undefined or Empty

var person = Null;
person.FirstName; // Bang -> NullReference Exception
~~~

Why should every have an exception!! Exception. An empty field or object or glas of water is not an exception. It has a defined state. Empty!!

*Example2:*

~~~
List aList;

aList.Count // Bang -> NullReference

Why a list is not Empty?

var aList = List.Empty;
var aList = []; // JavaScript Empty list in JavaScript

aList.Count // 0
aList.Select(x => x+1) // still an empty list


aList.FirstOrDefault(); // What is the default ?
aList.First(); // On an emtpy list is what?
~~~

## Why we use Null? ##

Because it is in the languages. And nobody think about if this should exists. Null was a mistake of ...
Some languages does not have the concept of Null.
Visual Basic:
VB is good because of the Variant Datatyp. A variable could IsNull or IsEmpty. JavaScript Example:

> a = {}
> a.b // undefined
> a.b = 3
> a.b // 3

## Lambda(OO) ##
The idea behind lambda(OO) is: Lambda means function. OO means object. The object are data. The function create, delete, change and convert data object.

~~~
var objB = func(objA);
var intA = convert(intStr);
~~~

## Lambda Cells ##
To get more robust code I tried to simulate a brain cell. With input values and an output value. If the imput changes the output is also changing according what the function of the cell is. Or you set the input values and invoke a calc to calculated the output.

*Example:*

~~~
class ConvertCell
{
	// Input
	string InputValue { private get; set; }
	
	// Output
	int OutputValue   { get; private set; }

	public ConvertCell()
	{
		InputValue = string.Empty;
		OutputValue = int.Empty; // or int.Undefined
	}
	
	// Input -> Output
	// Output = func(Input)
	public bool Calc()
	{
		if (string.IsEmpty(InputValue))
		{
			OutputValue = Int.Empty;
			return true; // Success state
		}
	
		int i;
		var success = int.TryParse(InputValue, out i);
		
		if (success)
		{
			OutputValue = i;
			return true; // Success state
		}
		
		return false; // Failed state
	}
}

var aCell = new ConvertCell() 
{
	InputValue = "123";
};

var success = aCell.Calc();

if (success) // on success the output value is valid
{
	Console.Write(aCell.OutputValue);
} 
else
{
	Console.Write("Conversion Failed");	
}
~~~

Can you imagine that a program exists of millions of small lambda-cells? There could be a "RangeCell". A Range cell has as input a start number and count and give you a list a numbers.

There could be a "AverageCell". A Average cell has as input a list of number and as output it gives you the average of this values. What cells you would like to have?

Think about cells like as small Lego(R) stones where you can build up a robust application.
Do you mean State or Exception?
If you have an operation is it always good to have a status code. On the status code you could react. There is not need for throwing exception. Because this is not an Exception. What is better?

~~~
var aString = "a123b";

var success = int.TryParse(aString, out i);
~~~

or

~~~
int.Parse(aString) // Bang!! Exception
~~~

Why is this an exception? The string you want to convert into an integer is not present an integer. I want to give example, I beliebe is not ok:

~~~
int a = int.Empty;
try
{
	a = int.Parse("12a3");
}
catch(Exception)
{
	// What to do here?
}
~~~

An exception is an exception something that is out of the rule. If an electric worker switch off the current and the computer goes out and you did not know it, this is an exception. Something that happend that you not expect. If you parse an integer the string could be a integer or not. So it is much better to give back the information successfully converted or not. Then you can act on that information.

## High Order Properties ##

~~~ 
class Person
{
	string LastName;
	string FirstName;
	double Height;
	double Weight;
}
~~~

or

~~~
class Person
{
	Name LastName; // This Properties are all Empty n
	Name FirstName;
	Length Height;
	Weight Weight;
}
~~~

## Values have Units ##

1m + 1mm = 1.001m or 1001mm

Angle  - Rad/Degree/Gon
Length - Meter/Centimeter/Millimeter/...
Time   - Hour/Second/Minutes

1sec + 1hours = 1h1sec;

ISO Units.
Importance of Layered Architecture

    User Interface Layer (GUI or CLI) (interface to human)
    Application Layer (create/delete/change data)
    DataStorage or Persistence Layer (load/store data) 

## Programmer Friendly Libraries ##

We often her the word user-friendly application. But what is you sit the whole day on the computer as programmer. A user of a computer the main task is to write program. To make user-friendly application you have to enjoy what you are doing. And to enjoy what you are doing, programming. You have to use programmer-friendly libraries and programming languages and tools. Programming is often very frustrating for instance if to have to write monoton code. If your library is not easy to handle. If things are not working as they should be and you does not have the source and could not debug why a thing is not happening. The best things you learn to code are very good example. A good example in the whole not only small part. To see how for instance a good 3-tier-application is working. Often die Developer-Network webside have only simple small peaces of stone but not the whole picture. And they are very often lack on good example. I do not believe that the best programmers write this documentation. I believe that hired middling are there to write shallow documentation examples. 
