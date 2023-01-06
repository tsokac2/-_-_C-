<h1 align="center">C# Basic Stuff</h1>

### Visual Studio ShortKeys

* Run: ```Ctrl + F5```
* Compile: ```Ctrl + Shift + B```



### Declaring Variables/Constants

int number;

int Numebr  = 1l

const float Pi = 3.14f; - float - data type

### Naming Conventions:

Camel Case: ```firstName``` - best option - ```int number;```
Pascal Case: ```FirstName``` - ```const int MaxZoom = 5;```
hungarian Notation: ```strFirstName```


### Primitive Types

![Primitive Types]()


### Non-Primitive Types
* String
* Array
* Enum
* Class


### Overflowing

```byte number = 255;```
number = number + 1; //0

checked
{
    byte number = 255;
    number = number + 1;
}


* ```byte``` is only **one** byte
* ```int``` is **4 bytes**


#### Scope


### Presenting data to the console
```
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            var number = 2;
            var count = 10;
            var totalPrice = 20.95f;
            var character = 'A';
            var firstName = "Tom";
            var isWorking = false;

            Console.WriteLine(number);

            Console.WriteLine(count);
            Console.WriteLine(totalPrice);
            Console.WriteLine(character);
            Console.WriteLine(firstName);
            Console.WriteLine(isWorking);
        }
    }
}
```

### Presenting Min and Max value of one byte and float

```
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("{0} {1}", byte.MinValue, byte.MaxValue);
            Console.WriteLine("{0} {1}", float.MinValue, float.MaxValue);
        }
    }
}
```

### Convert methods
* ToByte()
* ToInt16()
* ToInt32()
* ToInt64()


```
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            try
            {
                var number = "1234";
                int i = Convert.ToByte(number);
                Console.WriteLine(i);

            }
            catch (Exception)
            {

                Console.WriteLine("This will be showed on the console if you have an error");
            }

           
        }
    }
}

```

### C# Operators
* Arithmetic Operators
* Cpmparison Operators
* Assignment Operators
* Logical Operators
* Bitwise Operators

### Operators

#### Postfix Increment ```a++```
```int a = 1;```
```int b = a++```

//a = 2, b = 1

#### Prefix Increment ```++a```
```int a = 1;```
```int b = ++a```
// a = 2, b = 2

### Comments

#### single-line Comments

``` // Here is a single-line comment
int a = 1
```

#### Multi-line Comments
```
/*
Here is a multi-line comment
*/

int a = 1;
```


### Swapping the variables data example
```
namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            int num1;
            int num2;
            int temp;

            Console.Write("\nEnter the First Number: ");
            num1 = int.Parse(Console.ReadLine());

            Console.Write("\nEnter the Second Number: ");
            num2 = int.Parse(Console.ReadLine());

            temp = num1;
            Console.WriteLine(temp);
            num1 = num2;
            Console.WriteLine(num1);
            num2 = temp;
            Console.WriteLine(num2);
        }
    }
}
```