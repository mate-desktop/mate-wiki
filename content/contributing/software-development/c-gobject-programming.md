---
title: C Programming/GObject
weight: -10
---

Although written in C, most MATE applications are heavily based on Object Oriented Programming principles.

Since the C Programming-Language was not created with Object Oriented Programming in mind, it has no explicit support for classes, inheritance, polymorphism and other OO Concepts. Neither does it have its own Virtual Table, which is found in object-oriented languages such C++, Java and C#. Therefore, it might not be as easy to implement an object-oriented programming paradigm using only C's language features and standard library. However, it can be done using structures which contain both function pointers as well as data, for example, or by using third-party libraries.

There are many third-party libraries designed to add support for object-oriented programming in C. The most general-purpose and widely used among these is the GObject System, which is part of Glib. The GObject System comes with its own virtual table. To create an object in C using the GObject system, it has to be sub-classed from the GObject struct.

{{< toc >}}

## Object-Creation

In this example a new object will be implemented directly derived from GObject. For simplicity, the object is named MyObject.

### Declaring An Object

To create a simple non-derivable (final) object, two structs must be declared, the instance and the class. They are declared using a macro:

```c
/* in myobject.h */
G_DECLARE_FINAL_TYPE (MyObject, my_object, MY, OBJECT, GObject)
```

This declares two structures, `MyObject` and `MyObjectClass`. `MyObject` must be defined in the C implementation, and `MyObjectClass` is already defined by the macro.

### Boiler-Plate Code

Since the GObject System is just a third-party library and therefore cannot make any changes to the C Language itself, creating a new object requires a lot of boiler-plate code. This is mostly handled by the macro shown above. However, the following is also required:

```c
/* in myobject.h */
#define MY_TYPE_OBJECT my_object_get_type ()
```

The macro defines several functions, namely `MY_OBJECT ()` and `MY_OBJECT_CLASS ()`, used for casting, `MY_IS_OBJECT ()` and `MY_IS_OBJECT_CLASS ()` for testing whether an object or class is of the correct type and `MY_OBJECT_GET_CLASS ()` for getting the class structure from an instance.

### Defining The Object

Before use, the newly created object must be defined, along with the instance structure.

```c
/* in myobject.c */

struct _MyObject
{
    GObject parent_instance;

    /* other members */
};

G_DEFINE_TYPE (MyObject, my_object, G_TYPE_OBJECT)
```

### Static Functions

There are a few static functions that may or may not to be defined, depending on your object. For a minimal object these ones are compulsory:

```c
/* in myobject.c */
static void
my_object_class_init (MyObjectClass *klass)
{
     /* code */
}

static void
my_object_init (MyObject *self)
{
     /* code */
}
```

### The Constructor

There is no internal way of allocating memory for an object in C. Therefore an explicit constructor must be declared for the new object.

```c
/* in myobject.c */

GObject *
my_object_new (void)
{
     return g_object_new (MY_TYPE_OBJECT,
                          0);
}
```

### Object-Usage

Although creating the object using its own pointer-type is perfectly valid, it is recommended to use the pointer-type of the object at the top of the hierarchy i.e the furthest off base class. The newly created object may now be used like this:

```c
/* in main.c */

/* Note: GObject is at the top of the hierarchy. */

/* declaration and construction */
GObject *myobj = my_object_new ();

/* destruction */
g_object_unref (myobj);
```

## Inheritance

### Concept

Inheritance is one of the most widely used and useful OO Concepts. It provides an efficient way to reuse existing code by wrapping it up into an object and then sub-classing it. The new classes are known as derived classes. Many object hieriarchies can be created using inheritance. Inheritance is also one of the most efficient ways of abstracting code.
Implementation

In the GObject System, inheritance can be achieved by sub-classing GObject. Since C provides no keyword or operator for inheritance, a derived object is usually made by declaring the base instance and base class as a member of the derived instance and derived class respectively. In C code:

```c
/* derived object instance */
struct _DerivedObject
{
     /* the base instance is a member of the derived instance */
     BaseObject parent_instance;
};
```
-----

Source: https://en.wikibooks.org/wiki/C_Programming/GObject

