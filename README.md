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
 
