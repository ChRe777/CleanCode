# Clean Code

## Personal Notes

* People should enjoy coding.
* People should can read code.

## Tips

### Design

Design error always leads to unclean code. Clean design is import.
Design before start coding. Have a clear simple design. Not overcomplicate things at start time.

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

###Use intention-revealing names*


    int d; // elapsed time in days
    d ... means nothing instead use

    int elapsedTimeInDays;
    int daysSinceCreation;
    int daysSinceModification;

###Avoid disinformation

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

###Make Meaningful Distinctions

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

###Use searchable names

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
        

###Avoid encoding

    PhoneNumber phoneString; // name not changed if type changed
    
    private string m_desc; // the textual description
    
    Use ShapeFactory and ShapeFactoryImp instead of IShapeFactory and ShapeFactory
    
###Avoid Mental Mapping

###Class Names

Classes and objects should have noun or noun phrases like

* Customer 
* WikiPage 
* Account 
* AdressParser

Avoid words like *Manager*, *Processor*, *Calculator*, *Data* or *Info*

###Method Names

###Don't be cute

###Pick One Word per Concept

###Don't Pun

Do not use the same word for instance *add* for different things.

do not use add if you mean insert
do nit use add if you mean append

###Use Solution Domain Names

Uses computer science terms, algorithm names, patterns name, math terms and so on.
People who read your code are programmers.

AccountVisitor, JobQueue people should know what that means.

###Use Problem Domain Names

###Add Meaningful Context

###Don't Add Gratuitous Context

Dont not use a prefix for every class NSString NS for NextStep

Do not use

* customerAdress
* accountAdress

but use

    PostalAdress for a postal adress
    Mac for a mac adress
    URI for a web adress

