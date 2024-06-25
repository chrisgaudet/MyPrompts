Show me a class in C#

Sure, here's a simple example of a class in C#:
using System;

namespace ExampleNamespace
{
    public class Person
    {
        // Fields
        private string firstName;
        private string lastName;
        private int age;

        // Properties
        public string FirstName
        {
            get { return firstName; }
            set { firstName = value; }
        }

        public string LastName
        {
            get { return lastName; }
            set { lastName = value; }
        }

        public int Age
        {
            get { return age; }
            set
            {
                if (value >= 0)
                {
                    age = value;
                }
                else
                {
                    throw new ArgumentOutOfRangeException("Age cannot be negative");
                }
            }
        }

        // Constructor
        public Person(string firstName, string lastName, int age)
        {
            this.FirstName = firstName;
            this.LastName = lastName;
            this.Age = age;
        }

        // Method
        public void Introduce()
        {
            Console.WriteLine($"Hello, my name is {FirstName} {LastName} and I am {Age} years old.");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Create a new Person object
            Person person = new Person("John", "Doe", 30);

            // Call the Introduce method
            person.Introduce();
        }
    }
}
