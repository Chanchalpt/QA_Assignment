using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp21
{
    class Program
    {
        static void Main(string[] args)
        {
            string numberString;
            int num;
            //Taking user selections
            do
            {
                Console.WriteLine("1. Enter triangle dimension: ");
                Console.WriteLine("2. Exit");
                Console.Write("Enter your Selection: ");
                numberString = Console.ReadLine();
            } while (!(int.TryParse(numberString, out num)) || num < 0 || num > 3);
            //taking triangle sides from user input
                if (num == 1)
                {
                    Console.Write("Enter number one: ");
                    int numOne = int.Parse(Console.ReadLine());
                    Console.Write("Enter number two: ");
                    int numTwo = int.Parse(Console.ReadLine());
                    Console.Write("Enter number three: ");
                    int numThree = int.Parse(Console.ReadLine());
                    string result = TriangleSolver.Analyze(numOne, numTwo, numThree);
                    Console.WriteLine(result);
                }
                //for exiting program
                else if (num == 2)
                {
                    Environment.ExitCode = 5;
                }

                Console.ReadKey();
        }
    }
}
