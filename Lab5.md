
# Lab 5



## ArrayList Operations
### Steps:
1. Create an `ArrayList` for storing student names.
2. Perform operations like `Add`, `Remove`, `RemoveRange`, and `Clear`.

**Code:**
```csharp
using System.Collections;

ArrayList studentNames = new ArrayList();

// Add students
studentNames.Add("John");
studentNames.Add("Alice");
Console.WriteLine("After Adding: " + string.Join(", ", studentNames.ToArray()));

// Remove a student by index
studentNames.RemoveAt(1);
Console.WriteLine("After Removing: " + string.Join(", ", studentNames.ToArray()));

// Remove range
studentNames.AddRange(new string[] { "Alice", "Bob", "Charlie" });
studentNames.RemoveRange(0, 2);
Console.WriteLine("After Removing Range: " + string.Join(", ", studentNames.ToArray()));

// Clear all students
studentNames.Clear();
Console.WriteLine("After Clearing: Count = " + studentNames.Count);
```

---

## List Operations
### Steps:
1. Create a `List` for storing student names.
2. Perform operations like `Add`, `Remove`, `RemoveRange`, and `Clear`.

**Code:**
```csharp
using System.Collections.Generic;

List<string> studentNames = new List<string>();

// Add students
studentNames.Add("John");
studentNames.Add("Alice");
Console.WriteLine("After Adding: " + string.Join(", ", studentNames.ToArray()));

// Remove a student by index
studentNames.RemoveAt(1);
Console.WriteLine("After Removing: " + string.Join(", ", studentNames.ToArray()));

// Remove range
studentNames.AddRange(new List<string> { "Alice", "Bob", "Charlie" });
studentNames.RemoveRange(0, 2);
Console.WriteLine("After Removing Range: " + string.Join(", ", studentNames.ToArray()));

// Clear all students
studentNames.Clear();
Console.WriteLine("After Clearing: Count = " + studentNames.Count);
```

---

## Stack Operations
### Steps:
1. Create a `Stack` for storing integer values.
2. Perform operations like `Push`, `Pop`, `Peek`, `Contains`, and `Clear`.

**Code:**
```csharp
Stack<int> stack = new Stack<int>();

// Push items
stack.Push(10);
stack.Push(20);
Console.WriteLine("After Pushing: " + string.Join(", ", stack));

// Pop item
Console.WriteLine("Popped: " + stack.Pop());

// Peek item
Console.WriteLine("Peek: " + stack.Peek());

// Check contains
Console.WriteLine("Contains 20: " + stack.Contains(20));

// Clear items
stack.Clear();
Console.WriteLine("After Clearing: Count = " + stack.Count);
```

---

## Queue Operations
### Steps:
1. Create a `Queue` for storing integer values.
2. Perform operations like `Enqueue`, `Dequeue`, `Peek`, `Contains`, and `Clear`.

**Code:**
```csharp
Queue<int> queue = new Queue<int>();

// Enqueue items
queue.Enqueue(10);
queue.Enqueue(20);
Console.WriteLine("After Enqueuing: " + string.Join(", ", queue));

// Dequeue item
Console.WriteLine("Dequeued: " + queue.Dequeue());

// Peek item
Console.WriteLine("Peek: " + queue.Peek());

// Check contains
Console.WriteLine("Contains 20: " + queue.Contains(20));

// Clear items
queue.Clear();
Console.WriteLine("After Clearing: Count = " + queue.Count);
```

---

## Dictionary Operations
### Steps:
1. Create a `Dictionary` for storing key-value pairs.
2. Perform operations like `Add`, `Remove`, `ContainsKey`, `ContainsValue`, and `Clear`.

**Code:**
```csharp
Dictionary<int, string> students = new Dictionary<int, string>();

// Add key-value pairs
students.Add(1, "John");
students.Add(2, "Alice");
Console.WriteLine("After Adding: " + string.Join(", ", students.Select(kv => kv.Key + "=" + kv.Value)));

// Remove a key-value pair
students.Remove(1);
Console.WriteLine("After Removing: " + string.Join(", ", students.Select(kv => kv.Key + "=" + kv.Value)));

// Check key and value existence
Console.WriteLine("Contains Key 2: " + students.ContainsKey(2));
Console.WriteLine("Contains Value 'Alice': " + students.ContainsValue("Alice"));

// Clear dictionary
students.Clear();
Console.WriteLine("After Clearing: Count = " + students.Count);
```

---

## Hashtable Operations
### Steps:
1. Create a `Hashtable` for storing key-value pairs.
2. Perform operations like `Add`, `Remove`, `ContainsKey`, `ContainsValue`, and `Clear`.

**Code:**
```csharp
using System.Collections;

Hashtable students = new Hashtable();

// Add key-value pairs
students.Add(1, "John");
students.Add(2, "Alice");
Console.WriteLine("After Adding: " + string.Join(", ", students.Keys.Cast<int>().Select(k => k + "=" + students[k])));

// Remove a key-value pair
students.Remove(1);
Console.WriteLine("After Removing: " + string.Join(", ", students.Keys.Cast<int>().Select(k => k + "=" + students[k])));

// Check key and value existence
Console.WriteLine("Contains Key 2: " + students.ContainsKey(2));
Console.WriteLine("Contains Value 'Alice': " + students.ContainsValue("Alice"));

// Clear hashtable
students.Clear();
Console.WriteLine("After Clearing: Count = " + students.Count);
```

---
