# Static members

* Can be accessed directly by the class. It's not necessary to instantiate an object. It is true for data members and also for methods.
* A good example of the use of static is Singleton implementation.

# Interface vs Abstract Class

|        | Interface           | Abstract Class  |
| :-------------: |:-------------:| :-----:|
| **Methods**      | only abstract | abstract and non-abstract |
| **Variables**      | *no states*: only static final      | *stateful*: static, no-static, final, non-final |
| **Multiple Inheritance** | *Implement* multiple interfaces      | *Extend* only one Abstract Class   |

* First of all, an *Abstract Class* is a special type of class that can not be instantiated. 
* Remember that a subclass can extends only one *Abstract Class*, but can implement multiple *Interfaces*. 
* An *Abstract Class* can be partially implemented, an *Interface* only define the methods.

**C++**: allows multiple inheritance

# Virtual Methods

```cpp

Student * p = new Person();
p->f(); // Person

Student * p = new Programmer();
p->f(); // Person

/*
    Both cases call Person's method.
    This happens by static binding.
*/

class Person() {
    virtual void f() {
        // ...
    }
}

Student * p = new Person();
p->f(); // Person

Student * p = new Programmer();
p->f(); // Programmer

/*
    As the method has been declared as virtual, it will call the derived class method, dynamic binding. 

    WARNING! 
    In C++ and C#, you can declare a method as Virtual. In Java, all methods are Virtual by default.
*/

class Person() {
    virtual void f() = 0; 
}

/*
    Pure Virtual Methods are Virtual Methods that must be implemented inside derived classes.

    In Java and C#, they're calles abstract methods.
*/

```

# Overloading and Overriding

* **Overloading**: two methods with the same name, but the arguments or the function type are different.

* **Overriding**: same name, type, arguments. Different from super class implementation.
