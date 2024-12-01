
# **Lab-1**

---

## **Table of Contents**  
1. [Print Personal Details](#1-print-personal-details)  
2. [Input and Output Handling](#2-input-and-output-handling)  
3. [String Interpolation](#3-string-interpolation)  
4. [Area Calculations](#4-area-calculations)  
5. [Unit Conversions](#5-unit-conversions)

---

### **1. Print Personal Details**

**Objective:**  
Create a program to display your name, address, contact number, and city.

**Steps:**  
1. Declare string variables for `Name`, `Address`, `Contact`, and `City`.  
2. Assign values to these variables.  
3. Use `Console.WriteLine()` to display the output in a formatted way.

**Code:**

```csharp
using System;

class Program
{
    static void Main()
    {
        string name = "John Doe";
        string address = "123 Elm Street";
        string contact = "9876543210";
        string city = "New York";

        Console.WriteLine($"Name: {name}\nAddress: {address}\nContact: {contact}\nCity: {city}");
    }
}
```

---

### **2. Input and Output Handling**

**Objective:**  
Accept two numbers from the user and print them.

**Steps:**  
1. Use `Console.ReadLine()` to take user inputs for two numbers.  
2. Convert inputs to integers using `int.Parse()`.  
3. Print the numbers using `Console.WriteLine()`.

**Code:**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter the first number: ");
        int number1 = int.Parse(Console.ReadLine());

        Console.Write("Enter the second number: ");
        int number2 = int.Parse(Console.ReadLine());

        Console.WriteLine($"The entered numbers are {number1} and {number2}.");
    }
}
```

---

### **3. String Interpolation**

**Objective:**  
Prompt the user to input their name and country and display a formatted message.

**Steps:**  
1. Accept inputs for `Name` and `Country` using `Console.ReadLine()`.  
2. Use string interpolation (`$`) to format the output message.  
3. Display the output using `Console.WriteLine()`.

**Code:**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter your name: ");
        string name = Console.ReadLine();

        Console.Write("Enter your country: ");
        string country = Console.ReadLine();

        Console.WriteLine($"Hello {name} from country {country}!");
    }
}
```

---

### **4. Area Calculations**

**Objective:**  
Calculate the area of a square, rectangle, and circle.

**Steps:**  
1. Use formulas for area calculations:  
   - Square: `side * side`  
   - Rectangle: `length * width`  
   - Circle: `π * radius^2`  
2. Take inputs for dimensions using `Console.ReadLine()`.  
3. Perform calculations and display results.

**Code:**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter the side of the square: ");
        double side = double.Parse(Console.ReadLine());
        Console.WriteLine($"Area of Square: {side * side}");

        Console.Write("Enter the length of the rectangle: ");
        double length = double.Parse(Console.ReadLine());
        Console.Write("Enter the width of the rectangle: ");
        double width = double.Parse(Console.ReadLine());
        Console.WriteLine($"Area of Rectangle: {length * width}");

        Console.Write("Enter the radius of the circle: ");
        double radius = double.Parse(Console.ReadLine());
        Console.WriteLine($"Area of Circle: {Math.PI * radius * radius}");
    }
}
```

---

### **5. Unit Conversions**

**Objective:**  
Convert temperature between Celsius and Fahrenheit.

**Steps:**  
1. Use the formulas:  
   - Fahrenheit = `(Celsius * 9/5) + 32`  
   - Celsius = `(Fahrenheit - 32) * 5/9`  
2. Accept input and perform the conversion based on user choice.  
3. Display the result.

**Code:**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter 1 for Celsius to Fahrenheit or 2 for Fahrenheit to Celsius: ");
        int choice = int.Parse(Console.ReadLine());

        if (choice == 1)
        {
            Console.Write("Enter temperature in Celsius: ");
            double celsius = double.Parse(Console.ReadLine());
            Console.WriteLine($"Temperature in Fahrenheit: {(celsius * 9 / 5) + 32}");
        }
        else if (choice == 2)
        {
            Console.Write("Enter temperature in Fahrenheit: ");
            double fahrenheit = double.Parse(Console.ReadLine());
            Console.WriteLine($"Temperature in Celsius: {(fahrenheit - 32) * 5 / 9}");
        }
        else
        {
            Console.WriteLine("Invalid choice.");
        }
    }
}
```

---


