What is Object?
    Objects is called as instance of the class
    create many objects of the same class
    object test=new Class()


What is Encapsulation?
    process of binding the data members and member functions into a single unit


What is Abstraction?
    process of hiding the implementation details and displaying the essential features

** Encapsulation vs Abstraction

Which are Access Specifiers?
    5 access specifiers
    public
        can be accessible outside the class through object reference
    private
        can be accessible with in the class can't access outside class
    protected
        it like private class but accessible in derived classes also through member functions
    internal
        can be visible inside the assembly, Accessible through objects
    protected internal
        can be visible inside the assembly through objects,
        derived classes outside the assembly through member functions


What is Inheritance?
    process of deriving the new class from an already existing class(Base Class)
    class Car : Vehicle

How can you implement multiple inheritance in C#?
    Using Interfaces, you can implement multiple inheritance in C#.

Are private class members inherited to the derived class?
    Yes, the private members are also inherited 
    in the derived class but we will not be able to access them

What is Polymorphism?
    When a message can be processed in different ways it is called polymorphism
    2 types of polymorphism
         1) Compile time polymorphism also know as Overloading (Early Binding)
         2) Rub time polymorphism also know as OverRiding(Late Binding)


What is method Overloading?
    Creating multiple methods in a class with the same name 
    but with different parameters and different types is called method overloading.

When and why to use method Overloading?
    when you need a couple of methods that take different parameters

What is method Overriding?
    Overriding means to change the functionality of a method without changing the signature
    (i.e) method name,parameter, return type
    Derived class method will completely overrides base class method 
    i.e. when you refer base class object

    //Base  Class
    public class web {
    string name = "GeeksForGeeks";
        public virtual void showdata()
        {
            Console.WriteLine("Website Name: " + name);
        }
    }
    //derived  Class
    class stream : web {
    string s = "Computer Science";
        public override void showdata()
        {
            base.showdata();         
            Console.WriteLine("About: " + s);
        }
    }
    stream E = new stream();
    E.showdata();

    //"Website Name: " +"GeeksForGeeks"
    //"About: " +"Computer Science"

 
What is Constructor?
    1)Constructor is a special method of the class that will be 
    automatically invoked when an instance of the class is created
    2)The main use of constructors is to initialize private fields 
    of the class while creating an instance for the class
    3)When you have not created a constructor in the class, 
    the compiler will automatically create a default constructor in the class
    4)The default constructor initializes all numeric 
    fields in the class to zero and all string and object fields to null

Describe some of the key points regarding the Constructor.
    A constructor does not have any return type, not even void.
    A static constructor can not be a parameterized constructor.
    Within a class you can create only one static constructor.
    There are 5 types of constructors,
        1)Default Constructor
            A default constructor has every instance of the class to be initialized to the same values. The default constructor initializes all numeric fields to zero and all string and object fields to null inside a class
        2)Parameterized Constructor
            A constructor with at least one parameter is called a parameterized constructor. 
            To create instance to pass parameter,using construct assign value to private variable
        3)Copy Constructor
            The constructor which creates an object by copying variables from another object is called a copy constructor. The purpose of a copy constructor is to initialize a new instance to the values of an existing instance.
             
             employee emp1 = new employee("Vithal", 23); 
             employee emp2 = new employee(emp1);     

        4)Static Constructor
            When a constructor is created using a static keyword
            it will be invoked only once for all of the instances of the class and it is invoked during the creation of the first instance
            
            A static constructor cannot be called directly.
            does not take access modifiers or have parameters
        5)Private Constructor

What is Private Constructor?
    The main purpose of creating private constructor is to restrict 
    the class from being instantiated when it contains every member as static.

Can you create object of class with private constructor in C#?
    No

What is the use of private constructor in C#?
    It is used to stop object creation of a class.
    It is used in Singleton class.
    It is used to stop a class to be inherited.

What is the use of static constructor in C#?
    Static constructor is a special constructor that gets called before 
    the first object of the class is created

What is Destructor?
    A Destructor is automatically invoked when an object is finally destroyed.
    The name of the Destructor is the same as class and prefixed with a tilde (~).
    used to free the dynamic allocated memory and release the resources.

What is Namespaces?
    Allow creating a system to organize the code
    

What are Virtual, Override, and New keywords in C#?
    Virtual is used to modify a method, property, indexer, or event declared in the base class and allows it to be overridden in the derived class
   
    Override is used to extend or modify a virtual/abstract method, property, indexer, or event of the base class into the derived class.
    

What is the difference between Struct and Class in C#?
    Type
        Struct- It is value type
        Class- 	It is reference type
    Inherits from
        Struct- System.Value type
        Class- 	System.Class type
    Used for
        Struct- Small amount of data
        Class- 	large amount of data
    Inherited to
        Struct- not be inherited
        Class- 	inherited
    Abstract
        Struct- not ob abstract
        Class- 	abstract type
    Default constructor
        Struct- Do not have permission to create any default constructor
        Class- 	You can create a default constructor


What is Interface?
    An interface looks like a class, but it has no implementation.
    The only thing it contains is declarations of events, indexers, methods and/or properties
    The reason interfaces only provide declarations is because they are 
    inherited by structs and classes,which must provide an implementation for each interface member 
    declared.

Why to use Interfaces in C#?
    Extensibility
    Implementation Hiding
    Accessing object using interfaces
    Loose coupling
What is Implicit interface implementation?

What is Explicit interface implementation?


What is Abstract class?
    An abstract class is a special kind of class that can not be instantiated.
    An abstract class is only to be sub-classed (inherited from)
    It only allows other classes to inherit from it but can not be instantiated

Describe Abstract class in detail.
    You can not create an object of Abstract Class.
    An inheritance between abstract to abstract classes is possible. 
    An abstract class can never be sealed or static.
    An abstract member can not be static or private.
    An abstract method can not be marked virtual.
    The abstract keyword can be used with class, methods, properties, indexers and events.

What is the difference between Abstraction and Encapsulation?
    Encapsulation is wrapping, it's just hiding properties and methods.
    Encapsulation is used for hiding the code and data in a single unit to protect the data from the outside world.
    Class is the best example of encapsulation.
    Abstraction refers to showing only the necessary details to the intended user
Can Abstract class be Sealed in C#?
    No, an abstract class cannot be a sealed class.
Can abstract class have Constructors in C#?
    Yes, Abstract class can have constructor in C#.

Can you declare abstract methods as private in C#?
    No. Abstract methods cannot be private in C#.

Can abstract class have static methods in C#?
    Yes, Abstract class can have static methods in C#.

Does Abstract class support multiple Inheritance?
    No, Abstract class does not support multiple Inheritance.

Abstract class must have only abstract methods. Is it true or false?
    False. Abstract class can have both abstract and non abstract methods.

When do you use Abstract Class?

Why can Abstract class not be Instantiated?

Which type of members can you define in an Abstract class?
    You can define all static and non-static members
    including properties, fields, indexers and also abstract methods.

What is Operator Overloading?
    
Is it possible to restrict object creation in C#?
    Yes, it is possible to restrict object creation in C# by using following,
    Abstract Class
    Static Class
    Private or Protected Constructor

Can you inherit Enum in C#?
    Enums are by default sealed. So, you can not inherit them.

Is it possible to achieve Method extension using Interface?
    Yes, it is possible to achieve Method extension using Interface.

Is it possible that a Method can return multiple values at a time?
    Yes, it is it possible that a Method can return multiple values at a time in C# by using the following:
        KeyValue pair
        Ref or Out parameters
        Struct or Class
        Tuple


What is Constant?
    Constant is known as “const” keyword in C#.
    It is also known as immutable values.
    compile time and do not change their values at run time like in 
    any function or constructor for the life of application till the application is running.

What is Readonly?
    Readonly is known as “readonly” keyword in C#.
    It is also known immutable values.
    They are known at compile and run time and do not change their values at run time like in any function for the life of application till the application is running.
    You can assign their value by constructor when we call constructor with “new” keyword.

What is Static?
    The static keyword is used to specify a static member.
    Static keyword can be used with classes, fields, methods, properties, operators, events, and constructors
    If the static keyword is applied to a class, all the members of the class must be static.
    Static constructor cannot be parameterized

What is Static ReadOnly?
    Static Readonly type variable value can be assigned at runtime or at compile time and can be changed at runtime

Can “this” be used within a Static Method?
    No, “this” cannot be used within a static method.
    keyword 'this' returns a reference to the current instance of the class containing it.

What is Design Patterns in .Net & Types of Design Pattern??
    Object oriented world is a reusable solution to common software design problems
     Creational Patterns: 
        It mainly deals with creation of Objects and Classes.
    Structural Patterns: 
        It deals with Class and Object Composition.
    Behavioral Patterns: 
        It deals with Class and Object communication. That means they are concerned with the communication between class and objects.

Which ate the key Benefits of using Design Patterns?
    developer a selection of tried and tested solutions to work with

What is the difference between Static class and Singleton instance? 
   static 
    - not implement an interface
    - not clone the object 
    - static object stores in stack
    - static class is generally initialized when it is first loaded
   Singleton     
    - to implement an interface for some business reason or IoC purpose
    - clone the object of Singleton
    - Singleton object stores in heap
    - A singleton can be initialized lazily or asynchronously 

Can you serialize Hashtable?
    No, you can not serialize Hashtable.
    .NET Framework does not allow serialization of any object that 
    implements the IDictionary interface

Why is Singleton pattern considered an Anti-pattern?
    Memory allocated to a Singleton can not be freed.
    Singletons promote tight coupling between classes, so it is hard to test.

What is the use of Yield keyword in C#?
    Yield keyword helps you to do custom stateful full iteration 
        It helps to provide custom iteration without creating temp collections.
        
How to catch multiple exceptions at once in C#?
    You can catch multiple exceptions using condition statements in C#.

What is use of the IDisposable interface in C#?
    he primary use of the IDisposable interface is to clean up unmanaged resources.
    ”unmanaged” means things like database connections, sockets, etc.

What is Property in C#.net?
    Properties are members that provide a flexible mechanism to read, write or compute the values of private fields.
    It uses methods to access and assign values to private fields called accessors

What are accessors?
    The Get and Set portions or blocks of a property are called accessors.

What is Partial Class?
    A partial class is only used to split the definition of a class in two or more classes in a same source code file or more than one source files.
    
    You can create a class definition in multiple files but it will be compiled as one class at run time and also when you’ll create an instance of this class. So, you can access all the methods from all 
    source file with a same object.
    
    You can use “partial” keyword with all the class name which you want to bind together with the same name of class in same namespace.

What is Sealed Class?
    Sealed class is used to restrict the inheritance feature of object oriented programming.
    Sealed class is the last class in the hierarchy.
    Sealed class can be a derived class 
    structs and enum are sealed.
    
What is Sealed Methods and Properties?
    Sealed method is used to define the overriding level of a virtual method.
    Sealed keyword is always used with override keyword

How to call base class constructor from derived class in C#?
    Use base keyword for this type of initialization

What is base keyword?
    The base keyword is used to access members of the base class from within a derived class.

What are the Benefits of Three Tier Architecture?
    Reusability: You can reuse the middle layer with different user interfaces 
    like ASP.NET, windows etc.
        You can also reuse your DAL with different projects.
    
    Maintainability: When you change in one layer due to the
    modular approach it does not have ripple effect on other layers.
    
    You have to do less amount of changes 

What is the Difference between Design Patterns and Architectural Patterns?
    Design Patterns
        solving technical problems in a way that has proven it self many times
        Design structures and practices that make for creating reusable Object-Oriented software
        Design pattern examples are Factory Pattern, Singleton, Facade, State
    Architecture Patterns
        Software application architecture is the process of defining a structured solution
        patterns for solving software application architecture problems
        Examples of different Architectures might be MVC, MVVM, MVP, n-layer
        The architecture typically needs to be decided up front and often is difficult to change once the application is built.


What is Constructor Chaining in C#?
    Constructor Chaining is an approach where a 
    constructor calls another constructor in the same or base class.
What is the Difference between this and base in C#? 
    THIS refers to the current instance (not the “current class”).
    It can only be used in non-static methods/members. 
        Because, in a static method there is no current instance.
    Base:
        BASE is a keyword that allows inherited method call, 
        i.e. it calls the specified method from the base type.
        It calls the base method directly even if it is virtual.
        