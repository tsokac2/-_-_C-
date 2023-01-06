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