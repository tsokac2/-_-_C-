### 1. 99 bottles of beer

Simple count down with while loop

```
namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {

            int intBottles = 99;
            string strLineOne = "";
            string strLineTwo = "";

            string strBottles = "bottles";

            while (intBottles >= 0)
            {
                if(intBottles == 0)
                {
                    strLineOne = "No more bottles of beer on the wall. No more bottles of beer.";
                    strLineTwo = "Got to the store and buy some more";

                    Console.WriteLine(strLineOne);
                    Console.WriteLine(strLineTwo);

                    Console.ReadKey();

                    intBottles = 99; // this line will make it loop forever
                }

                //Change bottles to bottle when on 1 bottle is left

                if (intBottles == 1)
                {
                    strBottles = "bottle";
                }

                strLineOne = intBottles + " " + strBottles + " of beer on the wall,";
                strLineOne += intBottles + " " + strBottles + " of beer.";

                intBottles--;

                //Change bottles to bottle when on 1 bottle is left

                if (intBottles == 1)
                {
                    strBottles = "bottle";
                }
                if (intBottles == 0)
                {
                    strBottles = "bottles";
                }

                strLineTwo = "Take one down and pass it around. " + (intBottles);
                strLineTwo += " " + strBottles + " of beer on the wall";

                Console.WriteLine(strLineOne);
                Console.WriteLine(strLineTwo);
            }

            Console.ReadKey();
        }
    }
}
```

### 2. FizzBuzz

```
using System;
using System.Collections.Generic;

namespace HelloWorld
{
    class Program
    {

        public static List<int> GetIntegers()
        {
            var integerList = new List<int>();

            for (var i = 1; i <= 100; i++)
            {
                integerList.Add(i);
            }

            return integerList;
        }

        public static void FizzBuzz(List<int> integerList)
        {
            foreach(var item in integerList)
            {
                if(item % 3 == 0 && item % 5 == 0)
                {
                    Console.WriteLine("FizzBuzz");
                }
                else if (item % 3 == 0)
                {
                    Console.WriteLine("Fizz");
                }
                else if (item % 5 == 0)
                {
                    Console.WriteLine("Buzz");
                }
                else
                {
                    Console.WriteLine(item);
                }
            }
        }

        static void Main(string[] args)
        {

            var integerList = GetIntegers();

            FizzBuzz(integerList);
        }
    }
}
```

```
namespace FizzBuzz
{
    class Program
    {
        static void Main(string[] args)
        {
            for (int i = 1; i <= 100; i++ )
            {
                if(i % 15 == 0)
                {
                    Console.WriteLine("FizzBuzz");
                }
                else if (i % 3 == 0)
                {
                    Console.WriteLine("Fizz");
                }
                else if (i % 5 == 0)
                {
                    Console.WriteLine("Buzz");
                }
                else
                {
                    Console.WriteLine(i);
                }
            }
{

            }
        }
    }
}
```
