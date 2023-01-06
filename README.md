# Main Class Documentaion Template for C#

## Class-level attributes 
Description: Attributes are declarative tags that can be applied to certain language elements, such as classes or methods. They can be used to specify metadata about the element, such as how it should be serialized or whether it is visible to certain tools.

(such as the [Serializable] attribute) or other metadata that is associated with your class. 

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:

``` 
[Serializable]
public class MyClass
{
    // class implementation goes here
} 
```

---

## Enumertors
Description: An enumerator is a type that defines a set of named constants, typically used to represent a set of related values. For example, you might define an enumerator called "DaysOfTheWeek" with values "Monday", "Tuesday", etc.

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:

```
public enum DaysOfTheWeek
{
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
}
```



---




## Constructors:
Description: A constructor is a special method that is called when an instance of a class is created. It is typically used to initialize the instance variables of the new object. methods with the same name as the class that are used to create an instance of the class

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:
```
public class MyClass
{
    private int _id;
    private string _name;

    public MyClass(int id, string name)
    {
        _id = id;
        _name = name;
    }
}
```

* In this example, the MyClass class has a constructor that takes two arguments: an int for the id and a string for the name. The constructor initializes the _id and _name instance variables with the values passed in as arguments.
* The constructor has the same name as the class and is called when an instance of the class is created using the new keyword, like this:

```
MyClass obj = new MyClass(123, "John Smith");
```

* This creates a new MyClass object and initializes its _id and _name instance variables with the values 123 and "John Smith", respectively.

## Variables

Description: A variable is a storage location in memory that has a name and a type. It is used to hold data that can be accessed and modified by the program.

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
name: ```name```
type: ```type```
access modifier: ```access modifier```
###### Examples:
```
int age = 30;
string name = "John Smith";
bool isRegistered = true;
double balance = 123.45;
char initial = 'J';
```
In these examples, we are declaring variables of various types:
* `int`: an integer type that can hold whole numbers
* `string`: a string type that can hold a sequence of characters
* `bool`: a boolean type that can hold the values true or false
* double: a double-precision floating-point type that can hold decimal values
* `char`: a character type that can hold a single Unicode character

## Properties
Description: A property is a member of a class that represents a value that can be read or written. It is similar to a field, but it is accessed using get and set accessors rather than directly.

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
feilds:
access modifier:
get 
set
###### Examples:
```
public class MyClass
{
    private int _age;

    public int Age
    {
        get { return _age; }
        set { _age = value; }
    }
}
```

In this example, the `MyClass` class has a property called `Age` that is of type `int`. The property has a `get` accessor and a `set` accessor, which are used to get and set the value of the `_age` field, respectively.

The `get` accessor is used to return the value of the `_age` field when the property is accessed, and the `set` accessor is used to assign a new value to the `_age` field when the property is set.

Properties are typically used to provide access to private fields in a class, while hiding the implementation details of the field from the user of the class. They can also be used to perform validation or other processing when the property is set or accessed.


## Exceptions: 
Description: if your class or its methods can throw any exceptions, you should document them. An exception is an object that represents an error or exceptional condition that occurs during the execution of a program. Exceptions can be thrown by the program or by the runtime system, and they can be caught and handled by the program to allow it to continue 

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:
```
try
{
    int x = int.Parse("abc");
}
catch (FormatException ex)
{
    Console.WriteLine("An error occurred: {0}", ex.Message);
}
```

In this example, we are using a `try` block to enclose a block of code that might throw an exception. The code inside the try block attempts to parse the string ``"abc"`` as an integer using the `Parse` method of the `int` class. However, the string is not in a valid format for an integer, so the `Parse` method throws a FormatException.

The `catch` block catches the exception and handles it by printing an error message to the console. The `FormatException` object is passed to the catch block as an argument, and we can access its Message property to get the error message.

Exceptions are used to signal errors or exceptional conditions that occur during the execution of a program. They allow you to handle these errors in a structured way, rather than letting the program terminate abruptly.

## Methods
Description:  A method is a block of code that performs a specific task and optionally returns a value. It is a member of a class and can be called using an object of the class.

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
| name: ```name``` |
| arguments: ```arguments``` |
| access modifier: ```access modifier``` |
| return type: ```return type``` |
###### Examples:
```
public int Add(int x, int y)
{
    return x + y;
}
```

In this example, we have a method called `Add` that takes two `int` arguments, `x` and `y`, and returns their sum as an `int` value. The method consists of a single statement that returns the result of adding `x` and `y`.

Methods are used to encapsulate a piece of code that performs a specific task. They can be called from other parts of the program to execute the code they contain, and they can also return a value if needed.

Methods are typically used to break up a larger program into smaller, more manageable pieces, and to improve code reuse by allowing you to write a piece of code once and use it in multiple places.

## Overloaded methods: 
Description: if you have multiple methods with the same name but different signatures (arguments), you should document the different overloads. Overloaded methods are multiple methods with the same name but different signatures (number or types of arguments). They allow you to reuse the same method name in different contexts, depending on the arguments passed to the method.

---

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
| name: ```name``` |
| arguments: ```arguments``` |
###### Examples:
```
public int Add(int x, int y)
{
    return x + y;
}

public double Add(double x, double y)
{
    return x + y;
}

public decimal Add(decimal x, decimal y)
{
    return x + y;
}
```

In this example, we have three methods with the same name, `Add`, but each one has a different signature. The first method takes two `int` arguments and returns an `int` value, the second method takes two `double` arguments and returns a `double` value, and the third method takes two `decimal` arguments and returns a `decimal` value.

Because the methods have different signatures, they are considered to be overloaded. They can be called with arguments of the appropriate types, and the correct method will be called based on the types of the arguments.

Overloaded methods are useful when you want to perform the same operation on different types of data, or when you want to provide multiple versions of a method with different behavior.

## Indexers
Description: Indexers: An indexer is a member of a class that allows objects of that class to be indexed in a similar way to an array. It is accessed using the "[]" operator and can be used to get or set the value of an element in the class.

---
#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:
```
public class MyList
{
    private int[] items = new int[10];

    public int this[int index]
    {
        get { return items[index]; }
        set { items[index] = value; }
    }
}
```

In this example, we have a class called `MyList` that has a `private` field called `items` that is an array of `int` values. The class also has an indexer called `this` that allows objects of the class to be indexed like an array. The indexer has a `get` accessor and a `set` accessor, so it can be used to both retrieve and set the value of an element in the `items` array.

```
public class MyDictionary
{
    private Dictionary<string, int> items = new Dictionary<string, int>();

    public int this[string key]
    {
        get
        {
            if (items.ContainsKey(key))
            {
                return items[key];
            }
            else
            {
                return -1;
            }
        }
        set { items[key] = value; }
    }
}
```

In this example, we have a class called `MyDictionary` that has a `private` field called `items` that is a `Dictionary` object mapping `string` keys to `int` values. The class also has an indexer called `this` that allows objects of the class to be indexed using a `string` key. The indexer has a `get` accessor and a `set` accessor, so it can be used to both retrieve and set the value of an element in the `items` dictionary. The `get` accessor checks if the dictionary contains the specified key and returns the value if it does, or -1 if it does not. The `set` accessor simply sets the value of the element with the specified key.

## Delegates
Description: A delegate is a type that represents a reference to a method. It allows you to pass a method as an argument to another method, or to store it in a variable so it can be called later.

---

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:
```
public delegate int MyDelegate(int x, int y);

public class MyClass
{
    public static int Add(int x, int y)
    {
        return x + y;
    }

    public static int Subtract(int x, int y)
    {
        return x - y;
    }
}

public static void Main()
{
    MyDelegate del = new MyDelegate(MyClass.Add);
    int result = del(5, 3);
    Console.WriteLine(result); // Outputs 8

    del = new MyDelegate(MyClass.Subtract);
    result = del(5, 3);
    Console.WriteLine(result); // Outputs 2
}
```

In this example, we have a delegate called `MyDelegate` that takes two `int` arguments and returns an `int`. We also have a class called `MyClass` with two `static` methods, `Add` and `Subtract`, that both match the signature of the delegate.

In the `Main` method, we create an instance of the delegate called `del` and assign it to the `Add` method. We then call the delegate with the arguments `5` and `3`, and the result is printed to the console. Next, we assign the delegate to the `Subtract` method and call it again with the same arguments. The result is printed to the console again.

## Events
Description: An event is a mechanism for communication between objects in an application. It allows an object to notify other objects when something interesting happens, such as a button being clicked or a timer expiring.

---

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:
```
public class Timer
{
    public delegate void TickHandler(Timer timer, EventArgs e);
    public event TickHandler Tick;

    public void Start()
    {
        while (true)
        {
            // Fire the Tick event every second
            System.Threading.Thread.Sleep(1000);
            OnTick(new EventArgs());
        }
    }

    protected virtual void OnTick(EventArgs e)
    {
        if (Tick != null)
        {
            Tick(this, e);
        }
    }
}

public class Program
{
    static void Main(string[] args)
    {
        Timer timer = new Timer();
        timer.Tick += Timer_Tick;
        timer.Start();
    }

    private static void Timer_Tick(Timer timer, EventArgs e)
    {
        Console.WriteLine("Tick!");
    }
}
```

In this example, we have a `Timer` class that fires a `Tick` event every second. The `Tick` event is defined using a delegate called `TickHandler` and has an event handler called `Tick`.

In the `Main` method, we create an instance of the `Timer` class and assign a method called `Timer_Tick` as the event handler for the `Tick` event. Then we start the timer by calling the `Start` method.

The `Start` method enters an infinite loop and fires the `Tick` event every second by calling the `OnTick` method. The `OnTick` method checks if there are any event handlers registered for the `Tick` event, and if there are, it calls them.

In this example, the `Timer_Tick` method is the event handler that is registered for the `Tick` event. It simply writes the string "Tick!" to the console.

## Interfaces:
Description: a set of related methods that a class can choose to implement. An interface is a set of related methods that a class can choose to implement. It defines a contract that the class must follow, but does not provide any implementation for the methods.

--- 

#### Used In Project

---

##### Component name: ```code```
| Summary | 
| -------- | 
| Summary of component     |
###### Examples:
```
public interface IVehicle
{
    string Make { get; set; }
    string Model { get; set; }
    int Year { get; set; }
    int Speed { get; }

    void Start();
    void Stop();
    void Accelerate();
}

public class Car : IVehicle
{
    public string Make { get; set; }
    public string Model { get; set; }
    public int Year { get; set; }
    public int Speed { get; private set; }

    public Car(string make, string model, int year)
    {
        Make = make;
        Model = model;
        Year = year;
    }

    public void Start()
    {
        // Implementation details go here...
    }

    public void Stop()
    {
        // Implementation details go here...
    }

    public void Accelerate()
    {
        // Implementation details go here...
    }
}
```

In this example, we have an interface called `IVehicle` that defines a set of related methods that a class can choose to implement. It has four properties (`Make`, `Model`, `Year`, and `Speed`) and three methods (`Start`, `Stop`, and `Accelerate`).

We also have a class called `Car` that implements the `IVehicle` interface. This means that the `Car` class must provide an implementation for all of the methods and properties defined in the `IVehicle` interface.

The `Car` class has a constructor that takes three arguments (`make`, `model`, and `year`) and assigns them to the corresponding properties. It also provides an implementation for the three methods defined in the `IVehicle` interface.

---
