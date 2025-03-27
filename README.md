# Casting_And_Type_Conversions_CSharp
## TRY- CATCH BLOCK
```1. Using Try-Catch For Validation

while (true)
{
    try
    {
        Console.Write("Enter A Valid Integer: ");
        myNumber = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine($"It is a valid Number: {myNumber}");
        continue;           
    }
    catch (FormatException ex) 
    {
        Console.WriteLine(FormatException.Message);
        Console.WriteLine("Try Again\n");
        continue; 
    }
}
```

> **CASE:** User input tries to convert into **INT32** which will recognize values from –2147483648 through 2147483647. So either it gets that value or it goes into the **catch** block.
>
> This Type of Exception goes normally in **FormatException** as the format or type of data isn't correct.
>
> **Exception Message:** *Input string was not in a correct format.*
> 
> But when i try to check for values that is larger than **2147483647** or values smaller than **-2147483648**, the code breaks as FormatException doesn't guarantee message after the range of conversion (Convert.ToInt32) explodes.
>
> **Solution:** When i replace to basic **Exception**, it says that *Value was either too large or too small for an Int32* which works fine.
 

## 2. parse and TryParse
```
string name = "456554654";
bool k1 = int.TryParse(name, out int myNumber2);
Console.WriteLine($"TryParse Returned: {k1}");
Console.WriteLine($"My Number2 is : {myNumber2}");

 string name = "45655464465454";
 int k1 = int.Parse(name);
 Console.WriteLine(k1);
```
> **CASE:** datatype.Parse("4558241612382498") to parse form a data type to another if it is valid otherwise **SystemException** is generated.
>
> **CASE:** *bool getValidity = datatype.TryParse(Console.ReadLine(), out int num1)* to try to parse a data type to another and if it succeeds it returns true to **getValidity** and sets the value of **num1** to the parsed value. No **SystemException** is generated and all that gets returned is the **false** value.
>
> **Exception Message:** *Input string was not in a correct format.*
>

## 3. Comparison

| Parse        | TryParse           | 
| ------------- |:-------------:|
|Attempts to convert a string to a specific type (e.g., int.Parse, double.Parse).       | Attempts to convert a string to a specific type, similar to Parse.  | 
|Throws an exception: (e.g., FormatException, OverflowException) if the conversion fails.       | Returns a boolean value: indicating whether the conversion was successful.     |  
| Requires you to use a try-catch block for error handling.  | If the conversion fails, it returns false and the out parameter is set to its default value.    |   
||Eliminates the need for try-catch: for basic error handling. 
 
