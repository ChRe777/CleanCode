# Clean Code

## Notes

    People should enjoy coding.
    People should can read code.

### Meanful Names

> Rule: *Use intention-revealing names*


    int d; // elapsed time in days
    d ... means nothing instead use

    int elapsedTimeInDays;
    int daysSinceCreation;
    int daysSinceModification;

> Rule: *Avoid disinformation.*

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


> Rule: *Avoid words like 'Manager', 'Processor', 'Data' or 'Info'*
 
Bad examples are
- LayerManager
- ProductInfo
- ProductData

*ProductInfo* or *ProductData* are mean the same.
*Info* and *Data* are like Noise words like *a*, *an* and *the*.

> Rule: *The word 'variable', 'table', 'string' should never appear in a variable name.*

Examples: CustomerTable, errorString, firstVariable ...

> Rule: *Distinguish names in such a way that the reader knows what the differences offer*

There is a class Customer and a CustomerObject what is the distinct

    moneyAmount is indistinguishable from money
    customerInfo is -"- from customer
    account is -"- from accountData
    theMessage is -"- from message

> Rule: *Create searchable names*

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
        

> Rule: *Avoid encoding*

    PhoneNumber phoneString; // name not changed if type changed
    
    private string m_desc; // the textual description
    
    Use ShapeFactory and ShapeFactoryImp instead of IShapeFactory and ShapeFactory
    


