
# **Lab-2 (Class, Object, Constructors, Inheritance)**


## **Table of Contents**  
1. [Create a Class Candidate](#1-create-a-class-candidate)  
2. [Create a Class Staff](#2-create-a-class-staff)  
3. [Bank Account Class](#3-bank-account-class)  
4. [Student Class with Constructor](#4-student-class-with-constructor)  
5. [Rectangle Area Calculation Using Constructor](#5-rectangle-area-calculation-using-constructor)  

---

### **1. Create a Class Candidate**

**Objective:**  
Create a class named `Candidate` with properties like `ID`, `Name`, `Age`, `Weight`, and `Height`. Define member functions such as `GetCandidateDetails()` and `DisplayCandidateDetails()`.

**Steps:**  
1. Define a class with the required data members.  
2. Create functions to accept and display details.

**Code:**

```csharp
using System;

class Candidate
{
    public int ID;
    public string Name;
    public int Age;
    public double Weight;
    public double Height;

    public void GetCandidateDetails()
    {
        ID = 1;
        Name = "John Doe";
        Age = 25;
        Weight = 70.5;
        Height = 175.5;
    }

    public void DisplayCandidateDetails()
    {
        Console.WriteLine($"ID: {ID}, Name: {Name}, Age: {Age}, Weight: {Weight}, Height: {Height}");
    }
}

class Program
{
    static void Main()
    {
        Candidate candidate = new Candidate();
        candidate.GetCandidateDetails();
        candidate.DisplayCandidateDetails();
    }
}
```

---

### **2. Create a Class Staff**

**Objective:**  
Create a class `Staff` with properties such as `Name`, `Department`, `Designation`, `Experience`, and `Salary`. Accept data for 5 different staff members and display only the names and salaries of the staff who are **HOD**.

**Steps:**  
1. Define a class with the mentioned data members.  
2. Use `if` condition to check for the "HOD" designation and display the relevant information.

**Code:**

```csharp
using System;

class Staff
{
    public string Name;
    public string Department;
    public string Designation;
    public int Experience;
    public double Salary;
}

class Program
{
    static void Main()
    {
        Staff[] staffs = new Staff[5];
        for (int i = 0; i < 5; i++)
        {
            staffs[i] = new Staff();
            Console.Write("Enter Name: ");
            staffs[i].Name = Console.ReadLine();
            Console.Write("Enter Department: ");
            staffs[i].Department = Console.ReadLine();
            Console.Write("Enter Designation: ");
            staffs[i].Designation = Console.ReadLine();
            Console.Write("Enter Experience: ");
            staffs[i].Experience = int.Parse(Console.ReadLine());
            Console.Write("Enter Salary: ");
            staffs[i].Salary = double.Parse(Console.ReadLine());

            if (staffs[i].Designation.ToLower() == "hod")
            {
                Console.WriteLine($"Name: {staffs[i].Name}, Salary: {staffs[i].Salary}");
            }
        }
    }
}
```

---

### **3. Bank Account Class**

**Objective:**  
Create a `Bank_Account` class with data members like `Account_No`, `Email`, `User_Name`, `Account_Type`, and `Account_Balance`. Define member functions like `GetAccountDetails()` and `DisplayAccountDetails()`.

**Steps:**  
1. Define the data members for account details.  
2. Implement functions to accept and display account information.

**Code:**

```csharp
using System;

class Bank_Account
{
    public string Account_No;
    public string Email;
    public string User_Name;
    public string Account_Type;
    public double Account_Balance;

    public void GetAccountDetails()
    {
        Account_No = "12345";
        Email = "john@example.com";
        User_Name = "John Doe";
        Account_Type = "Savings";
        Account_Balance = 15000.50;
    }

    public void DisplayAccountDetails()
    {
        Console.WriteLine($"Account No: {Account_No}, Email: {Email}, Username: {User_Name}, Type: {Account_Type}, Balance: {Account_Balance}");
    }
}

class Program
{
    static void Main()
    {
        Bank_Account account = new Bank_Account();
        account.GetAccountDetails();
        account.DisplayAccountDetails();
    }
}
```

---

### **4. Student Class with Constructor**

**Objective:**  
Create a `Student` class with data members `Enrollment_No`, `Student_Name`, `Semester`, `CPI`, and `SPI`. Use a constructor to initialize the values and a member function `DisplayStudentDetails()`.

**Steps:**  
1. Define the class with the required data members.  
2. Use a constructor to initialize values.  
3. Implement a method to display details.

**Code:**

```csharp
using System;

class Student
{
    public int Enrollment_No;
    public string Student_Name;
    public int Semester;
    public double CPI;
    public double SPI;

    public Student(int enrollment_No, string student_Name, int semester, double cpi, double spi)
    {
        Enrollment_No = enrollment_No;
        Student_Name = student_Name;
        Semester = semester;
        CPI = cpi;
        SPI = spi;
    }

    public void DisplayStudentDetails()
    {
        Console.WriteLine($"Enrollment No: {Enrollment_No}, Name: {Student_Name}, Semester: {Semester}, CPI: {CPI}, SPI: {SPI}");
    }
}

class Program
{
    static void Main()
    {
        Student student = new Student(1001, "John Doe", 5, 8.7, 8.5);
        student.DisplayStudentDetails();
    }
}
```

---

### **5. Rectangle Area Calculation Using Constructor**

**Objective:**  
Calculate the area of a rectangle using a constructor.

**Steps:**  
1. Define a class with `length` and `width` as data members.  
2. Use a constructor to initialize them.  
3. Calculate the area using the formula `length * width`.

**Code:**

```csharp
using System;

class Rectangle
{
    public double Length;
    public double Width;

    public Rectangle(double length, double width)
    {
        Length = length;
        Width = width;
    }

    public void DisplayArea()
    {
        Console.WriteLine($"Area of Rectangle: {Length * Width}");
    }
}

class Program
{
    static void Main()
    {
        Rectangle rectangle = new Rectangle(10, 5);
        rectangle.DisplayArea();
    }
}
```

---
