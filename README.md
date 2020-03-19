# Prework-CodeChallenges
A repo for the prework code challenges

Even though Karina helped walk me through setup for some reason it isn't syncing. So that's great. Below is the code. 

using System;

namespace PreworkCodeChallenges
{
    class Program
    {
        static void Main(string[] args)
        {
            //ArrayMaxResult();
            //LeapYearCalc();
            Sequence();
        }

        static void ArrayMaxResult()
        {
            int[] maxArray = new int[5];
            Console.WriteLine("Enter five numbers between 1-10");
            for (int i = 0; i < 5; i++)
            {
                maxArray[i] = Convert.ToInt32(Console.ReadLine());
            }
            Console.WriteLine("Select a number from the list:");
            for (int i = 0; i < 5; i++)
            {
                Console.Write($"{maxArray[i]}, ");
            }
            int selected = Convert.ToInt32(Console.ReadLine());
            int count = 0;
            for (int i = 0; i < 5; i++)
            {
                if (maxArray[i] == selected)
                {
                    count++;
                }
            }
            Console.WriteLine($"Your score is {selected * count}");

        }

        static void LeapYearCalc()
        {
            Console.WriteLine("Enter a four digit year.");
            int year = Convert.ToInt32(Console.ReadLine());
            if (year % 4 == 0)
            {
                if (year % 100 != 0 || year % 400 == 0)
                {
                    Console.WriteLine($"{year} is a leap year.");
                }
            }
            Console.WriteLine($"{year} is not a leap year.");
        }

        static void Sequence()
        {
            int[] seqArray = new int[3]{1, 3, 2};
            int sum = 0;
            int multi = 1;
            Console.WriteLine($"Is this a perfect sequence?");
            for (int i = 0; i < seqArray.Length; i++)
            {
                Console.Write($"{seqArray[i]}, ");
                sum = sum + seqArray[i];
                multi = multi * seqArray[i];
            }
            if (sum == multi)
            {
                Console.WriteLine("Yes");
            }
            else Console.WriteLine("No");
        }
    }
}
