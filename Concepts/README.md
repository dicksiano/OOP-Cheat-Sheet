# Static members

* Can be accessed directly by the class. It's not necessary to instantiate an object. It is true for data members and also for methods.
* A good example of static 

# Virtual Methods

```cpp

Student * p = new Person();
p->f(); // Person

Student * p = new Programmer();
p->f(); // Person

/*
    Both cases call Person's method.
    This happens by static binding
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
    As the methods has been declared as virtual, it will call the derived class method, dynamic binding. 

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

* **Overloading**: two methods with the same name, but the arguments or the function type is different.

* **Overriding**: same name, type, arguments. Different from super class implementation.
