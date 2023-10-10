# Programowanie-obiektowe-
using System;

namespace laby1
{
    class Program
    {
        static void Main(string[] args)
        {
            //PoleKoła();
            //Zadanie1_2(2, 2);
            //Zadanie1_3(5);
            Zadanie1_6();
            //Zadanie1_5(1, -4, -5);
            Console.ReadLine();
        }
        static void PoleKoła()
        {
            Console.Write("Podaj promień: ");
            double r = Double.Parse(Console.ReadLine());
            double pole = r * Math.PI * r; Console.WriteLine("Pole wynosi: {0:0.##}", pole);
        }

        static void Zadanie1_2(int a, int b)
        {
            int pole = a * b;
            Console.WriteLine("Pole wynosi: " + pole);
            if (a == b)
            {
                Console.WriteLine("Prostokąt może być kwadratem");
            }
            else
            {
                Console.WriteLine("nie moze byc kwadratem");
            }
        }

        static void Zadanie1_3(int a)
        {
            if (a % 2 == 0)
            {
                Console.WriteLine("liczba jest parzysta");
            }
            else
            {
                Console.WriteLine("liczba jest nieparzysta");
            }
        }

        static void Zadanie1_4()
        {
            Console.WriteLine("podaj pierwsza liczbe:");
            int a = int.Parse(Console.ReadLine());
            Console.WriteLine("podaj druga liczbe:");
            int b = int.Parse(Console.ReadLine());
            Console.WriteLine("podaj trzecia liczbe:");
            int c = int.Parse(Console.ReadLine());

            int Max = Math.Max(a, Math.Max( b , c ));
            Console.WriteLine("najwieksza liczba: {0} ", Max);
            
        }

        static void Zadanie1_5(double a, double b, double c)
        {
            double x1, x2, re, im;
            
            double delta = b * b - 4 * a * c;
            if( delta > 0)
            {
                x1 = (-(b * b) - Math.Sqrt(delta))/ 2 * a;
                x2 = (-(b * b) + Math.Sqrt(delta))/ 2 * a;
                Console.WriteLine("pierwsiatkami rownania sa: " + x1 + " oraz " + x2);
            }
            if (delta == 0)
            {
                x1 = (-b) / 2 * a;
                Console.WriteLine("pierwiastkiem rownania kwadratowego jest: " + x1);
            }
            if (delta < 0)
            {
                im = Math.Sqrt(-(delta))/2*a;
                re = (-b) / 2 * a;
                Console.WriteLine("pierwsiatkami zespolonymi sa: " + re + "+" + im + "i oraz " + re + "-" + im + "i");
            }
        }

        static void Zadanie1_6()
        {
            double KursDolara = 4.33;
            double KursEuro = 4.57;
            double KursFranka = 4.77;

            Console.WriteLine("Podaj kwote w zl: ");
            double zlotowka = Double.Parse(Console.ReadLine());
            Console.WriteLine("wybierz interesujaca cie walute:\n1.Kurs Dolara\n2.Kurs Euro\n3.Kurs Franka Szwajcarskiego");
            int wybor = int.Parse(Console.ReadLine());
            double przelicznik;
            switch (wybor)
            {
                case 1:
                    przelicznik = zlotowka * KursDolara;
                    Console.WriteLine("Kwota do zaplaty: {0.00} zl", zlotowka);
                    break;
                case 2:
                    przelicznik = zlotowka * KursEuro;
                    Console.WriteLine("Kwota do zaplaty: {0.00} zl", zlotowka);
                    break;
                case 3:
                    przelicznik = zlotowka * KursFranka;
                    Console.WriteLine("Kwota do zaplaty: {0.00} zl", zlotowka);
                    break;
                default: Console.WriteLine("niepoprawna waluta");
                    break;

            }

        }
    }
}


