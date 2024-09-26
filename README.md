using System;


/*
 *  калькулятор
 */

namespace калькулятор
{
    internal class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Clear();
                double firstVaule, secondVaule;
                string action;

                try
                {
                    Console.WriteLine("введите число 1 ");
                    firstVaule = double.Parse(Console.ReadLine());

                    Console.WriteLine("введите число 2 ");
                    secondVaule = double.Parse(Console.ReadLine());
                }
                catch (Exception)
                {
                    Console.WriteLine("неудалось проеобразовать строкy в число! ");
                    Console.ReadLine();
                    continue;
                }


                Console.WriteLine("введите операцию '+' '-' '*' '/' ");
                action = Console.ReadLine();

                switch (action)
                {
                    case "+":
                        Console.WriteLine(firstVaule + secondVaule);
                        break;
                    case "-":
                        Console.WriteLine(firstVaule - secondVaule);
                        break;
                    case "*":
                        Console.WriteLine(firstVaule * secondVaule);
                        break;
                    case "/":
                        if (secondVaule == 0)
                        {
                            Console.WriteLine(0);
                        }
                        else
                        {
                            Console.WriteLine(firstVaule / secondVaule);
                        }


                        break;
                    default:
                        Console.WriteLine("Ошибка неизвестное действие! ");
                        break;
                }
                Console.ReadLine();

            }
        }
    }
}

