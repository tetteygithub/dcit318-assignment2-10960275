using System;

namespace AbstractClassDemo
{
    abstract class Shape
    {
        public abstract double GetArea();
    }

    class Circle : Shape
    {
        private double radius;

        public Circle(double radius)
        {
            this.radius = radius;
        }

        public override double GetArea()
        {
            return Math.PI * radius * radius;
        }
    }

    class Rectangle : Shape
    {
        private double length;
        private double breadth;

        public Rectangle(double length, double breadth)
        {
            this.length = length;
            this.breadth = breadth;
        }

        public override double GetArea()
        {
            return length * breadth;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Shape circle = new Circle(7);
            Shape rectangle = new Rectangle(7, 3);

            Console.WriteLine($"Circle Area: {circle.GetArea()}");    // Output: Circle Area: 78.53981633974483
            Console.WriteLine($"Rectangle Area: {rectangle.GetArea()}");  // Output: Rectangle Area: 24
        }
    }
}