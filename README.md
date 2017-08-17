
# Clean Code

This is not theory. This came from pratical working.

## My Service

I can take a program with a lot of messed up and complicated code and simplify it and still run efficiently.

With this website you can learn it to do it yourself. Or you let me do it for you and I charge you per line of code.

## Prologue

It must be clear said that unclean code is a fruit (of a problem). This site give some hints to clean up your code, but you also have to deal with why that happened. 

You have to find the root of this problem, otherwise you cleanup code and perhaps new unclean code will come back.
In the book "The Psychology of Computer Programming" from Author Gerald M. Weinberg is a good book that deals with some subjects.

"Programming is social ativity of a  group of people with different kind of skills,  but especially with different human behaviours that has nothing to with coding."

In this book Weinberg created a subject "Egoless programming".

This is a style of computer programming in which personal factors are minimized so that quality may be improved.

## Rules

Every rule in clean code is based on two rules:

* Keep it simple as possible
* Do it with love

Keep it simple seems to be hard for many people because
they learned/trained to think complicated. It is a matter
how your mindset is configured. So this is a thing to
overcome to change your thinking from complicated one to
a keep it simple thinking one. But this can be done.

## Main Reason

"You already know what I want you to know."

I compare it with learn to write a proper letters in school in your first class.
A teacher you knows how to write proper letters teach you how to write proper letters.
You get a class book where you can see how proper letter looks like. So you know the end result.
And you exercise to write proper letters by drawing it over a template letter in your book.
On an exercise sheet you repaint a semitransparent letter. And you do this very often.

The reason for that it that your brain is a neuronal network. 
You need to train and train it consciously until it goes into you subconscious mind.

So most people never learned how to write proper code (class, methods, functions) they are basically learned it autodidact. 
They read some book but never exercise it proper. By only rewrite a proper code that already.

## Solution 

Do it write and slow. Look how other API have done. 

Better to copy good then to fall into a trap. 
Be a disciple of some other a good code(er(s)).

## Knowing your business

You also have to know your business. You can not write a good program or library, if you do not know
what this program should do. If you can not do your business on paper, you can do write a proper program
for that business.

## Plan

You need a plan. Each house is build with a plan. A plan is important that you know how the end result
should look like. If you have no plan of the endresult you build another "Kowloon Walled City".
https://en.wikipedia.org/wiki/Kowloon_Walled_City

They build and build and build and the end result has to be destroyed from goverment because
it is dangerous to live there.

A Plan is important to have an overview. Otherwise you end in a mess and feel lost in the cost.
If the many people over many years work on a software without plan then the end result is a
"Kowloon Walled City"-like software.

A plan should have different kind of levels in detail. For instance a blockdiagram
of the components. And then this components as extra plan in more details. You go
from the big overview in to next level of details and the next and so on.

## Architecture

For a rough plan or architecture you can google for instance
 - Multitier architecture
 - Client–server model

Please do not invent the wheel again. Find a good example with a good architecture and learn from
the generation before. Do not fall into the trap you know how to build it.

## API

Write an open, extensional, flexible API.

If you have follower coders after you, they are must write in youe style.
Otherwise the software should does not work. Have an internal code and a public API.
Write a good documentation. The best way to teach is giving very
good example. Not only simple examples (like MDNs of languages or frameworks) 
but real and good pratical examples. Show the write how you wrote proper code
be open. Not hide it from others.

## Hindrances to overcome

* Attitude to be willingness to change and understand what I do is not good
* Bad Authorities at work or at school (but you can learn yourself at home)
* Lazyness (you know you are wrong, but you does not want to change and pay the price to change)


## Reasons (or excuses) for unclean code

* Time pressure
* Unclean enviroment
* Existing unclean code you have to work with
* Unprofessionell authority or enviroment
* Everyone code like he wants - Slang programming
* Untalented

Many people are under pressure at work so they do their
work not in love, but we fear what is the opposite of love.

Some my work in the branch for money and not called to ne
in that job. So it is hard for them and they are always
struggeling.

If you have 5 programmer and give them the same requirements
for a simple task you get probably the 5 different solutions.
Even when you have the same language used and the same
enviroment.

I compare it with "pitching" english. Every group create
his own slang to communicate. But if you have a single
programmer that has his own slang, it is later hard to
grow up with new people because they are not used of this
programming slang.

That why he a standards in language and we should also have
standard in programming. Not only how to write functions
but also how to right and design an application in general.

If you find out that you have no talent to write clean code
perhaps you have no calling on your life to be a programmer.
If I not talented in singing I can train myself how much I
want but I will never be a good singer.

## Personal Notes

* People should enjoy coding.
* People should can read the code.
* People should can maintain the code.
* People should can envolve the code.

## Tips

### Bugs

A lot of bugs a also a fruit or a sign that your application is not healthy
or unclean. Like in a unclean building where bugs (for instance cockroach) 
can grow easily. A log of bugs that come again back for instance from branching
and merging is a sign of unstable core classes. Your software has not rigid body
(no stable bones).

### Attitude

Writing clean code has to do with your attitude. Everything can be learned.
Some people believe that thre unclean code is ok and it is hard to change
their minds. So your attitude and willigness to change is very important.

### Source Control System

In old source control system you could choose the option that a file is locked
during editing and another one could not edit this file at the same time. 
So if you wanted to edit the same file you have to talk with this person.
The advantages is that communication between developers are triggered.

If you create clean code you should have small class or files. Why you ever need 
to mess around in others classes at the same time and then handle complicated merge conflicts, 
where you possible build in errors or break others code.

### Rigid body

Every software should be envolvable and for this it is need some that
is solid(rigid) like bones in a body and something the is soft and flexible
like your flesh and joints. Joints help to be flexible.
If you have no stable API or stable classes which give your application
the stability, you change no envolve (be flexible and be bending) if the
situation around the application is changing.
I worked in a project where this datastructure and classes that should
be stable are always changed in each release. So your software always loose
stability. Which brings stress to the whole team and the POs and bosses.

### Design

Design error always leads to unclean code. Clean design is import.
Design before start coding. Have a clear simple design. Not overcomplicate things at start time.

Code should be abstract and have rules in it. If your code have only exceptions of this rules
then you can not abstract it and the code will ugly and unclean. Unclean code is often a sign
for unclean design, unclean concept, unclean requirments. Tracing the root of the problem.

### Keep it simple (is a must)

If you realize that things get more and more complicated then its time to refactor.
This is very important for your future survival. Keep it simple at every stage.
And you have to believe that a very complex software can made out of simple building
stone in every level.

Think in lego term. Basis lego stones are simple stone. Imagine you build bigger
stones out of smaller simple stones. The bigger stones are also simple. And then
build with the bigger stone much bigger stones. They are again simple. But with
this stone your building is growing fast.

## API Thinking

Start to think more API-like. Create your classes for more then only one application.
Create a plugin concept on that API. Your API interface should be stable and not change
to often.

An api is the stable part of your system, where plugin or other classes the flexible part
application. To survive you need like your body stable bones and flexible parts to change
if the situation changes.

Today in agile enviroment we change everything everytim what make the system unstable
because there is no stable core anymore.

### Plugin

Often successful software has the ability to extend the application by plugins or
scripting languages. This is very important because you could not change the application
if the users needs change in future. The core of the application should be stable and
very generic designed. If you have a lot of experience over 20-30 years you will notice
that many application works the same inside indepent of the domain of the application.

## Think in Layers

It is very important to seperate layers at least use 3 layers.
Keep it as simple as possible.

* Storage Layer
* Business Layer (API)
* User Interface Layer

For instance a Business Layer and Storage Layer should be scriptable
and work without any user interface (graphical or console or whatever).

## Meanful Names

### Use intention-revealing names

    int d; // elapsed time in days
    d ... means nothing instead use

    int elapsedTimeInDays;
    int daysSinceCreation;
    int daysSinceModification;

### Avoid disinformation

Do not say *accountList* for grouping of accounts, say *accountGroup* or *accounts* for instance.

> Rule: *Do not use 'i', 'j' or 'k' in loops.*

Use for instance *index* instead of *i* if *i* means index.
Or use *rowIndex* or *columnIndex* instead of *i* and *j*.

    for(int i = 0; i < 5; i++)
    for(int index = 0; index < COUNT_ITEMS; index++)

    if (cell[STATUS_VALUE] == FLAGGED) { ... }
    if (cell.isFlagged()) { ... }

    public static copyChars(char[] a1, char[] a2) { ... }
    public statix copyChars(char[] source, char[] destination) { ... }

### Make Meaningful Distinctions

> Rule: *Avoid words like 'Manager', 'Processor', 'Data' or 'Info'*
 
Bad examples are:

* LayerManager
* ProductInfo
* ProductData

*ProductInfo* or *ProductData* are mean the same.
*Info* and *Data* are like Noise words like *a*, *an* and *the*.

> Rule: *The word 'variable', 'table', 'string' should never appear in a variable name.*

Examples are:

* customerTable
* errorString
* countVariable

Distinguish names in such a way that the reader knows what the differences offer

There is a class *Customer* and a *CustomerObject* what is the distinct?

Examples are:

* moneyAmount is indistinguishable from money
* customerInfo is -"- from customer
* account is -"- from accountData
* theMessage is -"- from message

### Use searchable names

    for (int j=0; j<34; j++)
    {
        s += (t[j]*4)/5;
    }
        
    for (in j=0; j < numberOfTasks; j++)
    {
        int realTaskDays = taskEstimate[j] * realDaysPerIdealDay;
        int realTaskWeeks = (realdays / WORK_DAYS_PER_WEEK);
        sum += realTaskWeeks;
    }     
        

### Avoid encoding

    PhoneNumber phoneString; // name not changed if type changed
    
    private string m_desc; // the textual description
    
    Use ShapeFactory and ShapeFactoryImp instead of IShapeFactory and ShapeFactory
    
### Avoid Mental Mapping

### Class Names

Classes and objects should have noun or noun phrases like

* Customer 
* WikiPage 
* Account 
* AdressParser

Avoid words like *Manager*, *Processor*, *Calculator*, *Data* or *Info*

### Method Names

### Don't be cute

### Pick One Word per Concept

### Don't Pun

Do not use the same word for instance *add* for different things.

do not use add if you mean insert
do nit use add if you mean append

### Use Solution Domain Names

Uses computer science terms, algorithm names, patterns name, math terms and so on.
People who read your code are programmers.

AccountVisitor, JobQueue people should know what that means.

### Use Problem Domain Names

### Add Meaningful Context

### Don't Add Gratuitous Context

Dont not use a prefix for every class NSString NS for NextStep

Do not use

* customerAdress
* accountAdress

but use

    PostalAdress for a postal adress
    Mac for a mac adress
    URI for a web adress
    
## Functions

Functions area *verbs* and classes are *nouns*.
Functions have a *hierarchy*. 

Each level in that hierarchy is a *level of abstraction*.

It is a *tree of functions* that tell a story. [Picture of a Tree]

Basically you use function to *create a language* with your own verbs and noun to
*tell the story* of what is going on the programm.

If you follow the rules your functions will be *short*, *well namend* and *nicely organized*.

### Just do it (without fear)

Write first a unclean function that breaks all the rules and 
then redesign until it follows the rules.

Writing good function is an ongoing learning process.
Write the functions how good to you can to follow the rules. 

Rewrite the functions until it follows the rules.

Write a big function. Rewrite it by extract functions. 
Write long parameter list. Write a class for this parameters.
Break your long function into levels.

### Rules

* Functions should be small
* Functions doing one thing
* Functions have descriptive names
* Functions should name with a verb-noun pair
* Functions arguments should one or max two
* Functions represent one level of abstraction
* Functions should have an input and return an output - y = f(x)

### Examples

    function int[] addNumber(int number) {
        return numbers.add(number);
    }

if you have to pass more then one parameter make a class (noun).
if you have to return more then one parameter make a class (noun).

For instance a simple sinus function

    sinusAlpha = sin(alpha)
    
turns an angle the sinus of that angle.

Functions convert, create, change, add, delete, ...

deleteKey, addPage, renderHtml, createPoint, convertInteger, ...

Point:

createPoint, deletePoint (= inverse of createPoint)
movePoint  (change)
point.setX (change)
point.getX (do not change)

convertInteger (change from a to b)

Functions converting nouns.
Functions creating objects/nouns.
Functions changing (= action/verbs) state of system (= nouns).

# Comments

Comments in the code are not api documentation of methods
or functions.

## Reason for Comments

* Your function does not do what they say they do in their name
* Peace of code does not do what they say they do in their name

## Experience - API Documentation

I also believe that code should be mostly self explaning.

Comments are often used to create a documentation of an API.

My experience is that example in this Developer Network API
Documentation leads to unclean code. Because they are based
on to simple examples. Where for instance the whole code of
a DB layer, a Controller or Presenter or View Logic code is
all together in the view for instance inside a handler of
a command clich event. A young developer my think that is the
way we should write code and end up in a mess. Because
later we learn you use for instance a MVC or MVP Patter or
what ever to oranize our code, that it is seperate in different
layer or classes.

## Misleading comments

I agree that it is better to name the function in the way
that you know what this function is doing then to write
a comment above the funciton. That's why a function
should do only one thing. Otherwise your function name must
be very very long :-) and explain all the things it is doing
in a very long name.

## Objects and data structures

Objects hides data and expose behavior.
Data structure expose data and have no behavior.

o = Lambda(o)

### Law of Demeter

A module should not know about the innards of the *objects* it manipulates.

A method *f* of class *C* only call:

- (a) *C*
- (b) An object created by *f*
- (c) An object passed as an argument to *f*
- (d) An object held in an instance variable of *C*

    class C
    {
        obj instVar

        func f(arg)
        {
            this.g()    // (a)
            arg.A       // (c)
            instVar     // (d)
        }
    
        func g(arg)
        {
            var obj = f(arg) // (b)
            f(obj)   
        }
    }

# Error Handling

A software is basically a set of rules.
Every rule has exceptions of that rules.

Or we can says a software have a normal flow and
if something exceptional happens with have to deal with
that otherwise our software will not very robust.

The software will not survive and fall into a state
where we have to restart the software.

A robust software *have to* deal with things that went wrong. 
Per definition if something can went wrong and you can not deal
with that you are not good in survival.

## NULL

What is the problem with NULL which is so common in most language.

I think this is best explained[^2] by the Inventor Tony Hoare[^1] himself.

But basically it is a value that has no type and has too much meanings.

[^1] https://de.wikipedia.org/wiki/Tony_Hoare
[^2] https://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare

### Don't *Return* NULL

* This is what we all do right?
* Do you believe, if it is ok to return NULL Pointer?

Normally we want to pass a special state. I want
to give back on object or an state that object is not there.

For instance in a factory you create objects but for one
reason you could not create the object and what you want give
back is the information you could not create the object.
Because input parameters are not valid of an error our whatever.

class Car
{
    Color Color;
    int   Wheels;
}

class SpecialCar : Car
{
}

class EmptyCar : Car
{
    EmptyCar 
    { 
        Color = transparent; // invisible - A car that is not made is can not be seen
        Wheels = 0;
    }
}

Instead of NULL to a List return an empty List.

### Don't *Pass* NULL

* This is what we all also do right?
* Do you believe, if it is ok to pass NULL Pointer?

What I saw with modern languages you even do not see
if the variable you pass is a reference type or a value type.

So in the old days in C++ you have to check in the beginning
of a function of the variable is NULL before you access a
method or property of the object. Otherwise you fall on the nose
and the program abort. Which does not lead to very robust software right?

I often say if God has build our body like with build software, we
all will not survive very long.

## *Unit* testing

The most important part if you want to have unit tests, you need to learn units.
A unit is a small part (like an electronic) that has a define input and output.
To make this happen it is really important to keep a unit small and simple.
I say this again keep it simple. Most people can not keep things simple because
of their complicated tinking mind set. If you learned over the year to think
complicated that this is normal for you and you can not think a simple way anymore.
Even if you want. You have to unlearn many things and must give your brain cells
a fresh start. By put all your think away what you know and put it on the self.
Then start fresh like someone you does not understand.
















