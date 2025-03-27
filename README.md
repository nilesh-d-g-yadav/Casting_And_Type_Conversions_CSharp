## Arrays In C#

# How Arrays are stored in C#
>
> You can store multiple variables of the same type in an array data structure. You declare an array by specifying the type of its elements.
>
>If you want the array to store elements of any type, you can specify object as its type.
>
>
```
    int[] numbers = {1,2,3,4,5,6};
```
```
    int[] newArr2 = new int[newArr2.length];
```
> An array can be single-dimensional, multidimensional, or jagged.
>
> The number of dimensions are set when an array variable is declared. The length of each dimension is established when the array instance is created. These values can't be changed during the lifetime of the instance.
>
> To loop over an array:
>
```
string[] weekDays = { "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" };
    foreach (string i in weekDays) { 
        Console.WriteLine($"{i}");
    }
```
> Types of Arrays are:
>
> **1. Single-dimensional Array in C#**
```
    int[] numbers = new int[] { 1, 2, 3, 4, 5, 6,7,8,9,10 };
```
>
> **2. Multi-dimensional Array in C#**
```
    int[,] array2DDeclaration = new int[4, 2];
```
> **3. Jagged Array in C#**
> ```
    
```
>Arrays can have more than one dimension. For example, the following declarations create four arrays. Two arrays have have two dimensions. Two arrays have three dimensions.
>
>Multi-dimensional arrays in C# are arrays that hold data in more than one dimension, allowing for efficient storage and manipulation of complex data structures. Unlike one-dimensional arrays, these arrays can be thought of as matrices or tables, providing rows and columns to organize and access elements based on multiple indices.
