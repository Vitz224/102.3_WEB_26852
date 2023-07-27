using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace question4
{
    internal class FindValues
    {
    }
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Welcome to the Circle Calculator!");

            // Read the radius from the user
            Console.Write("Enter the radius of the circle: ");
            string radiusInput = Console.ReadLine();

            // Parse the input to get the radius as a double
            if (double.TryParse(radiusInput, out double radius))
            {
                // Create an object of the FindValues class
                FindValues calculator = new FindValues();

                // Call the FindArea and FindCircumference methods with the user-given radius
                double area = calculator.FindArea(radius);
                double circumference = calculator.FindCircumference(radius);

                // Print the results
                Console.WriteLine($"Area of the circle: {area:F2}");
                Console.WriteLine($"Circumference of the circle: {circumference:F2}");
            }
            else
            {
                Console.WriteLine("Invalid input. Please enter a valid number for the radius.");
            }

            // Keep the console window open until the user presses a key
            Console.WriteLine("\nPress any key to exit.");
            Console.Readline();
        }
    }
}
