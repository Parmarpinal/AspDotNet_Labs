# Method Overloading and Method Overriding

## 1. Method Overloading

**Definition**:  
Method Overloading is a feature in object-oriented programming where multiple methods in the same class can have the same name but differ in:
- The number of parameters
- The type of parameters
- The order of parameters

**Key Points**:
- Methods must have the same name but differ in their parameter list.
- Method Overloading is resolved at compile time (Compile-time Polymorphism).

**Syntax**:
```csharp
class ClassName
{
    public void MethodName(int param1) 
    { 
        // Logic for one integer parameter 
    }

    public void MethodName(float param1) 
    { 
        // Logic for one float parameter 
    }

    public void MethodName(int param1, int param2) 
    { 
        // Logic for two integer parameters 
    }
}
```

**Example**:
```csharp
class Calculator
{
    public int Add(int a, int b) 
    {
        return a + b; // Adds two integers
    }

    public float Add(float a, float b) 
    {
        return a + b; // Adds two floats
    }

    public int Add(int a, int b, int c) 
    {
        return a + b + c; // Adds three integers
    }
}

// Usage:
Calculator calc = new Calculator();
Console.WriteLine(calc.Add(5, 10));        // Output: 15
Console.WriteLine(calc.Add(5.5f, 10.3f)); // Output: 15.8
Console.WriteLine(calc.Add(1, 2, 3));     // Output: 6
```

# Method Overriding

**Definition**:  
Method Overriding is a feature in object-oriented programming where a method in a derived class has the same name, return type, and parameters as in its base class, but provides a different implementation.

**Key Points**:
- Requires inheritance.
- The derived class method must use the `override` keyword.
- Method Overriding is resolved at runtime (Runtime Polymorphism).

**Syntax**:
```csharp
class BaseClass
{
    public virtual void MethodName() 
    {
        // Logic for base class implementation
    }
}

class DerivedClass : BaseClass
{
    public override void MethodName() 
    {
        // Logic for derived class implementation
    }
}
```

**Example**:
```csharp
class RBI
{
    public virtual void CalculateInterest()
    {
        Console.WriteLine("Interest as per RBI guidelines.");
    }
}

class HDFC : RBI
{
    public override void CalculateInterest()
    {
        Console.WriteLine("HDFC's specific interest rate calculation.");
    }
}

class SBI : RBI
{
    public override void CalculateInterest()
    {
        Console.WriteLine("SBI's specific interest rate calculation.");
    }
}

// Usage:
RBI bank;
bank = new HDFC();
bank.CalculateInterest(); // Output: HDFC's specific interest rate calculation.

bank = new SBI();
bank.CalculateInterest(); // Output: SBI's specific interest rate calculation.
```