using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                float S = 0;
                float[] Numbers = new float[3];
                try
                {
                    Console.WriteLine("Vvedite storony a");
                    Numbers[0] = float.Parse(Console.ReadLine());
                    Console.WriteLine("Vvedite storony b");
                    Numbers[1] = float.Parse(Console.ReadLine());
                    Console.WriteLine("Vvedite storony c");
                    Numbers[2] = float.Parse(Console.ReadLine());
                    var orderNumbers = from i in Numbers orderby i select i;
                    S = (float)1 / 2 * orderNumbers.ElementAt(0) * orderNumbers.ElementAt(1);
                    Console.WriteLine("Ploshad treugolnika ravna: "+S.ToString());
                    Console.ReadLine();
                    break;
                }
                catch { Console.WriteLine("Error try again: "); continue; }
            }
        }
    }
}
