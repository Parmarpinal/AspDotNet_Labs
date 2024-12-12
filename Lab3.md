
# Lab 3



---

## Table of Contents
1. [Exception Handling](#exception-handling)
   - [Divide by Zero Exception](#divide-by-zero-exception)
   - [IndexOutOfRange Exception](#indexoutofrange-exception)
2. [Abstraction](#abstraction)
   - [Abstract Class Implementation](#abstract-class-implementation)
3. [Interfaces](#interfaces)
   - [Addition and Subtraction](#addition-and-subtraction)
   - [Area Calculation](#area-calculation)
4. [String Functions](#string-functions)
   - [Common String Methods](#common-string-methods)
   - [Case Conversion](#case-conversion)
   - [Longest Word in String](#longest-word-in-string)

---

## Exception Handling

### Divide by Zero Exception
**Steps:**
1. Create a `try-catch` block to handle the `DivideByZeroException`.
2. Perform division and ensure that the divisor is checked.
3. Print a message when the exception is caught.

**Code:**
```csharp
try {
    int a = 10, b = 0;
    Console.WriteLine(a / b);
} catch (DivideByZeroException ex) {
    Console.WriteLine("Exception caught: " + ex.Message);
}
```

---

### IndexOutOfRange Exception
**Steps:**
1. Create an array of size 5 and read input from the user.
2. Attempt to access an index out of range in a `try-catch` block.
3. Handle the exception gracefully.

**Code:**
```csharp
try {
    int[] numbers = new int[5];
    for (int i = 0; i < 5; i++) {
        Console.Write($"Enter number {i + 1}: ");
        numbers[i] = int.Parse(Console.ReadLine());
    }
    Console.WriteLine(numbers[10]); // Intentional out-of-range access
} catch (IndexOutOfRangeException ex) {
    Console.WriteLine("Exception caught: " + ex.Message);
}
```

---

## Abstraction

### Abstract Class Implementation
**Steps:**
1. Create an abstract class `Sum` with two abstract methods: `SumOfTwo` and `SumOfThree`.
2. Extend the `Sum` class in another class `Calculate`.
3. Implement the abstract methods in the `Calculate` class.

**Code:**
```csharp
abstract class Sum {
    public abstract int SumOfTwo(int a, int b);
    public abstract int SumOfThree(int a, int b, int c);
}

class Calculate : Sum {
    public override int SumOfTwo(int a, int b) {
        return a + b;
    }

    public override int SumOfThree(int a, int b, int c) {
        return a + b + c;
    }
}

class Program {
    static void Main() {
        Calculate calc = new Calculate();
        Console.WriteLine("Sum of Two: " + calc.SumOfTwo(3, 7));
        Console.WriteLine("Sum of Three: " + calc.SumOfThree(3, 7, 5));
    }
}
```

---

## Interfaces

### Addition and Subtraction
**Steps:**
1. Create an interface `Calculate` with methods `Addition` and `Subtraction`.
2. Implement this interface in a class `Result`.
3. Perform addition and subtraction operations in the implemented methods.

**Code:**
```csharp
interface Calculate {
    int Addition(int a, int b);
    int Subtraction(int a, int b);
}

class Result : Calculate {
    public int Addition(int a, int b) {
        return a + b;
    }

    public int Subtraction(int a, int b) {
        return a - b;
    }
}

class Program {
    static void Main() {
        Result result = new Result();
        Console.WriteLine("Addition: " + result.Addition(10, 5));
        Console.WriteLine("Subtraction: " + result.Subtraction(10, 5));
    }
}
```

---

## String Functions

### Common String Methods
**Steps:**
1. Create a string and demonstrate methods like `Length`, `Substring`, `IndexOf`, etc.
2. Show examples with detailed comments in code.

**Code:**
```csharp
class Program {
    static void Main() {
        string str = "Hello, World!";
        Console.WriteLine("Length: " + str.Length);
        Console.WriteLine("Substring: " + str.Substring(0, 5));
        Console.WriteLine("Index of 'World': " + str.IndexOf("World"));
        Console.WriteLine("Replace: " + str.Replace("World", "C#"));
    }
}
```

---

### Case Conversion
**Steps:**
1. Accept a string from the user.
2. Replace lowercase characters with uppercase and vice versa.
3. Print the converted string.

**Code:**
```csharp
class Program {
    static void Main() {
        Console.Write("Enter a string: ");
        string input = Console.ReadLine();
        string converted = string.Concat(input.Select(c => char.IsLower(c) ? char.ToUpper(c) : char.ToLower(c)));
        Console.WriteLine("Converted String: " + converted);
    }
}
```

---

### Longest Word in String
**Steps:**
1. Accept a sentence from the user.
2. Split the string into words and find the longest one.
3. Display the longest word.

**Code:**
```csharp
class Program {
    static void Main() {
        Console.Write("Enter a sentence: ");
        string sentence = Console.ReadLine();
        string[] words = sentence.Split(' ');
        string longest = words.OrderByDescending(w => w.Length).FirstOrDefault();
        Console.WriteLine("Longest Word: " + longest);
    }
}
```
