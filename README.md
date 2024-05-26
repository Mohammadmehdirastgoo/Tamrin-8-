using System;

class Program
{
    public static void Main(string[] args)
    {
        Console.WriteLine("Enter a number");
        int number = int.Parse(Console.ReadLine());
        
        if (number > 0)
            Console.WriteLine("the number 2 times the entered number equals to: " + power1(number)); 
        
        if (number < 0)
            Console.WriteLine("the number 2 times the entered number equals to: " + power2(number));
        
        if (number == 0)
            Console.WriteLine("the number 2 times the entered number equals to 1");
        
        Console.WriteLine("Press any key to continue..."); 
        Console.ReadKey();
    }
public static int power1(int number)
{
    if (number > 1)
    {
        return 2 * power1(number - 1);
    }
    else
    {
        return 2;
    }
}

public static double power2(int number)
{
    if (number < 0)
    {
        return 2 / power2(number + 1);
    }
    else
    {
        return 2;
    }
}   
