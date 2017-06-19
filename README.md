using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_Six
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());
            int m = int.Parse(Console.ReadLine());
            int l = int.Parse(Console.ReadLine());
            int specialNum = int.Parse(Console.ReadLine());
            int controlNum = int.Parse(Console.ReadLine());

            int a = 0;
            int b = 0;
            int c = 0;

            int total = 0;
            int special = specialNum;

            for (int u = n; u >= 1; u--)
            {
                a = u;

                for (int j = m; j >= 1; j--)
                {
                    b = j;

                    for (int i = l; i >= 1; i--)
                    {
                        c = i;
            int sum = (a * 100) + (b * 10) + c;
                        total = sum;

                        if (total % 3 == 0)
                        {
                            special += 5;
                        }
                        else if (total % 5 == 0)
                        {
                            special -= 2;
                        }
                        else if (total % 2 == 0)
                        {
                            special *= 2;
                        }
                                                
                        if (special >= controlNum)
                        {
                            break;
                        }
                    }


                    if (special >= controlNum)
                    {
                        break;
                    }
                }


                if (special >= controlNum)
                {
                    break;
                }
            }

            if (special >= controlNum)
            {
                Console.WriteLine("Yes! Control number was reached! Current special number is {0}.", special);
            }
            else
            {
                Console.WriteLine("No! {0} is the last reached special number.", special);
            }
        }
    }
}
