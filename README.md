using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp21
{
    //TriangleSolver Class 
    public class TriangleSolver
    {
        //Analyze function
        public static string Analyze(int one, int two, int three)
        {
            //testing for equilateral triangle
            if (one == two && two == three)
            {
                return "It forms a equilateral triangle.";
            }
            //testing for Isosceles triangle
            else if (one == two || two == three || one == three)
            {
                return "It forms a Isosceles triangle.";
            }
            //testing for scalene triangle and triangle cannot be formed
            else
            {
                if (one >= two)
                {
                    if (one >= three)
                    {
                        if (one <(two + three))
                        {
                            return "It forms a scalene triangle.";
                        }
                        else
                        {
                            return "Cannot form a triangle.";
                        }
                    }
                    else
                    {
                        if (three < (one + two))
                        {
                            return "It forms a scalene triangle.";
                        }
                        else
                        {
                            return "Cannot form a triangle.";
                        }
                    }
                }
                else
                {
                    if (two >= three)
                    {
                        if (two < (one + three))
                        {
                            return "It forms a scalene triangle.";
                        }
                        else
                        {
                            return "Cannot form a triangle.";
                        }
                    }
                    else
                    {
                        if (three <(one + two))
                        {
                            return "It forms a scalene triangle.";
                        }
                        else
                        {
                            return "Cannot form a triangle.";
                        }
                    }
                }
            }
        }
    }
}
