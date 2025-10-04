# OOP

## **Introduction:**

Imagine you have a toy box full of toys. Each toy in the box is different, but they all have some things in common. For example, they all have a name, a color, and a shape. They can also do different things, such as roll, spin, or make noise.

Object-oriented programming (OOP) is a way of writing computer code that is similar to playing with toys. In OOP, you create objects that have properties and behaviors. Properties are like the things that describe the toy, such as its name, color, and shape. Behaviors are like the things that the toy can do, such as roll, spin, or make noise.

For example, you could create an object class called Toy. This class would have properties like name, color, and shape. It would also have behaviors like roll(), spin(), and makeNoise().

Once you have created the Toy class, you can create instances of the class. Each instance will be a unique toy with its own properties and behaviors. For example, you could create a Car instance with the name “Red Racer”. The Car instance would have the roll(), spin(), and makeNoise() behaviors, but it would also have its own unique behaviors, such as drive() and stop().

## **So What is OOP?**

Object-oriented programming (OOP) is a programming style that uses objects and their interactions to design applications and computer programs. OOP is one of the most popular programming styles used today.

## **Benefits of OOP?**

- Reduced code complexity: OOP can help to reduce the complexity of your code by making it more modular and reusable.
- Improved code quality: OOP can help to improve the quality of your code by making it more secure, testable, and maintainable.
- Increased programmer productivity: OOP can help to increase programmer productivity by making it easier to write, debug, and maintain code.
- Reduced development costs: OOP can help to reduce development costs by making it easier to reuse code and by reducing the amount of time required to develop and maintain software.

## **The Concept of Class and object:**

Classes and objects are the fundamental building blocks of OOP.

A class is a blueprint for creating objects. It defines the properties and behaviors that all objects of that class will have.

An object is an instance of a class. It has the properties and behaviors that are defined by the class.

ِ example: A car class might have the properties `color`, `make`, and `model`. It might also have the behaviors `drive()`, `stop()`, and `steer()`. You could use the car class to create many different car objects, such as a red Toyota Camry or a blue BMW X5.

## **What is Constructor and Destructor?**

constructor is a special method that is used to initialize an object. It is called when an object is created. The constructor can be used to set the initial values of the object’s properties.

destructor is a special method that is used to clean up an object before it is destroyed. It is called when an object is deinitialized. The destructor can be used to release any resources that are being used by the object.

## **Now Let’s clarify all last concepts by the code:**

```swift
class Car {
    //properties
    var color: String
    var make: String
    var model: String

    // constructor
    init(color: String, make: String, model: String) {
        self.color = color
        self.make = make
        self.model = model
    }

    //destructor
    deinit {
        print("The car is being destroyed.")
    }

    //behavior
    func drive() {
        print("drive")
    }
}

// Create a new car object
let redToyotaCamry = Car(color: "red", make: "Toyota", model: "Camry")

//Accessing properties and calling behaviors
let carColor = redToyotaCamry.color
redToyotaCamry.drive()

```

**Some additional information about constructor:**

- You can have multiple constructors for a class.
- Constructors can be designated or convenience initializers.
- Designated initializers must call one of their superclass’s designated initializers.
- Convenience initializers can call a designated initializer from their own class.

**Some additional information about** destructor**:**

- You can only have one destructor for a class.
- Destructors must be marked with the `deinit` keyword.
- Destructors are called in the reverse order that constructors are called.

## **OOP Concepts:**

![](https://miro.medium.com/v2/resize:fit:1400/0*R0SG9oPT-yu2vB6a.png)

## **1- Encapsulation:**

Encapsulation is a way of organizing code so that the implementation details of a class or struct are hidden from its users. This makes code more modular, reusable, and maintainable.

Imagine a car as a class. The car has many different parts, such as an engine, transmission, and wheels. The user of the car doesn’t need to know how all of these parts work together to make the car move. They just need to know how to drive the car.

The car class encapsulates all of the implementation details of the car. The user doesn’t need to know how the engine works, how the transmission works, or how the wheels work. They just need to know how to start the car, put it in gear, and steer it.

### **How to implement encapsulation:**

We can implement encapsulation by use this following techniques:

- Access control: Access control allows you to control which parts of your code are accessible to other parts of your code. You can use access control to hide the implementation details of your classes and structs from their users.
- Private properties and methods: Private properties and methods are only accessible to the class or struct in which they are defined. This makes them ideal for encapsulating the implementation details of your objects.
- Public interfaces: Public interfaces are the parts of your code that are exposed to other parts of your code. They should be designed carefully to provide users with access to the functionality of your objects without exposing the underlying implementation details.

### **Example:**

```swift
class Car {
    private var engine: Engine = Engine()

    func drive() {
        engine.start()
        print("The car is driving.")
    }

    func stop() {
        engine.stop()
        print("The car is stopped.")
    }
}

class Engine {
    func start() {
        print("The engine is starting.")
    }

    func stop() {
        print("The engine is stopping.")
    }
}

// Create a new car object
let car = Car()

// Start the car
car.drive()

// Stop the car
car.stop()
```

> In this example, the Car class encapsulates the Engine class. The Engine class's properties and methods are private, so they can only be accessed by the Car class. The Car class exposes a public interface that allows users to drive and stop the car without having to worry about the underlying implementation details.
> 

### **Benefits of encapsulation:**

- Modularity: Encapsulation helps to modularize code by breaking it down into smaller, more manageable pieces.
- Reusability: Encapsulation makes code more reusable by allowing you to hide the implementation details of an object from its users.
- Maintainability: Encapsulation makes code more maintainable by making it easier to change the implementation of an object without affecting its users.
- Security: Encapsulation can help to improve the security of your code by hiding sensitive implementation details from attackers.

### **Access modifiers:**

Access modifiers allow you to control which parts of your code are accessible to other parts of your code. This can help you to protect your data and make your code more modular and reusable.

Imagine a house with different rooms. Each room has a door that can be locked or unlocked. You can use the door lock to control who has access to each room.

Similarly, you can use access modifiers to control who has access to different parts of your code. For example, you can use access modifiers to hide your private data from other parts of your code, or to make your public functions accessible to other parts of your code.

Another real-life example of access modifiers is a bank account. Your bank account number and PIN are private information that should only be accessible to you and your bank. The bank uses access modifiers to protect your account information from unauthorized access.

Types of access modifiers ((in Swift)):

- `open`: Open access modifiers are the most permissive, and allow any code to access the corresponding properties and methods.
- `public`: Public access modifiers allow any code within the same module to access the corresponding properties and methods.
- `internal`: Internal access modifiers are the default access level in Swift, and allow any code within the same module to access the corresponding properties and methods.
- `fileprivate`: Fileprivate access modifiers allow any code within the same file to access the corresponding properties and methods.
- `private`: Private access modifiers are the most restrictive, and only allow the code within the same class or struct to access the corresponding properties and methods.

### **How to use access modifiers:**

To use access modifiers you simply need to add the access modifier keyword to the corresponding property or method declaration. For example, the following code shows how to declare a private property and a public method:

```swift
class Person {
    private var name: String

    public func getName() -> String {
        return name
    }
}
```

> In this example, the name property is private, which means that it can only be accessed by the Person class. The getName() method is public, which means that it can be accessed by any code within the same module.
> 

### **Getter and Setter Methods:**

Getter and setter methods are special methods that allow you to get and set the values of properties. Getter methods simply return the value of a property, while setter methods allow you to set the value of a property.

Example of getter and setter methods is a bank account. Your bank account has a balance, which is a property. You can use a getter method to check your balance, and a setter method to deposit or withdraw money from your account.

```swift
class BankAccount {
    private var balance: Double

    init(balance: Double) {
        self.balance = balance
    }

    // Getter method for the balance property
    func getBalance() -> Double {
        return balance
    }

    // Setter method for the balance property
    func setBalance(newBalance: Double) {
        balance = newBalance
    }

    // Deposit money into the account
    func deposit(amount: Double) {
        balance += amount
    }

    // Withdraw money from the account
    func withdraw(amount: Double) throws {
        if balance < amount {
            throw BankAccountError.insufficientFunds
        }

        balance -= amount
    }
}

enum BankAccountError: Error {
    case insufficientFunds
}

// Example usage:

let bankAccount = BankAccount(balance: 100)

// Get the balance
let balance = bankAccount.getBalance()

// Deposit money
bankAccount.deposit(amount: 50)

// Withdraw money
try bankAccount.withdraw(amount: 25)

// Print the new balance
print(bankAccount.getBalance()) // 125
```

### **Encapsulation vs Data Hiding:**

Encapsulation and data hiding are two related concepts in object-oriented programming (OOP), but they are not the same thing.

Encapsulation is the process of wrapping data and code together into a single unit, called a class or struct. This makes the data and code easier to manage, reuse, and protect.

Data hiding is the practice of making data inaccessible to other parts of the program, except through the methods of the class or struct that owns the data. This helps to protect the data from being corrupted or accidentally modified.

An example of encapsulation and data hiding is a car. The car encapsulates the data and code necessary to drive the car. The driver doesn’t need to know how the car works to drive it. They just need to know how to steer, accelerate, and brake.

The car also uses data hiding to protect the driver from being exposed to the hazardous components of the car, such as the engine and transmission. The driver can’t open the hood of the car while it is running, and they can’t reach the internal components of the car.

## **2- Inheritance:**

Inheritance is a fundamental concept of object-oriented programming that allows you to create new classes based on existing classes. This allows you to reuse code and create hierarchies of classes.

Imagine a car class. A car class has many different properties and behaviors, such as color, make, model, and the ability to drive and stop.

You could create a new class called `Truck` that inherits from the `Car` class. The `Truck` class would have all of the same properties and behaviors as the `Car` class, plus any additional properties and behaviors that are specific to trucks, such as a bed and the ability to tow trailers.

Another example of inheritance is a dog class. A dog class has many different properties and behaviors, such as name, breed, color, and the ability to bark and wag its tail.

You could create a new class called `Poodle` that inherits from the `Dog` class. The `Poodle` class would have all of the same properties and behaviors as the `Dog` class, plus any additional properties and behaviors that are specific to poodles, such as curly hair and the ability to perform tricks.

### **How to implement inheritance:**

To implement inheritance you use the `class` keyword. For example, the following code shows how to create a `Truck` class that inherits from the `Car` class:

```swift
class Car {
    var color: String
    var make: String
    var model: String

    func drive() {
        print("The car is driving.")
    }
}

class Truck: Car {
    var bed: Bed

    init(color: String, make: String, model: String, bed: Bed) {
        super.init(color: color, make: make, model: model)
        self.bed = bed
    }
}

let truck = Truck(color: "red", make: "Ford", model: "F-150", bed: Bed())

truck.drive()
```

> The super.init() method calls the initializer of the superclass, which is the Car class in this case.
> 

### **Benefits of inheritance:**

- Reuse of code: Inheritance allows you to reuse code by creating new classes that inherit from existing classes. This can save you time and effort when developing software.
- Hierarchy of classes: Inheritance allows you to create hierarchies of classes. This can make your code more organized and easier to understand.

## **3- Polymorphism:**

Polymorphism is the ability of a program to process objects that are of different types but share a common superclass. This allows you to write code that is more flexible and reusable.

Imagine a shape class. A shape class has many different properties and behaviors, such as color, size, and the ability to be drawn.

You could create new classes that inherit from the shape class, such as a circle class, a square class, and a triangle class. Each of these classes would have its own unique properties and behaviors, but they would all share the common superclass of shape.

This would allow you to write code that can work with all types of shapes, without having to write specific code for each type of shape. For example, you could write a function that draws any type of shape, regardless of its specific type.

Another example of polymorphism is a vehicle class. A vehicle class has many different properties and behaviors, such as color, make, model, and the ability to move.

You could create new classes that inherit from the vehicle class, such as a car class, a truck class, and a motorcycle class. Each of these classes would have its own unique properties and behaviors, but they would all share the common superclass of vehicle.

This would allow you to write code that can work with all types of vehicles, without having to write specific code for each type of vehicle. For example, you could write a function that drives any type of vehicle, regardless of its specific type.

### **How to implement polymorphism:**

To implement polymorphism you can use the following techniques:

- Method overloading: Method overloading allows you to define multiple methods with the same name, but with different signatures. The compiler will automatically call the correct method based on the type of the object that is being called.
- Method overriding: Method overriding allows you to redefine a method that is inherited from a parent class. This allows you to implement different functionality for the method for different types of objects.

### **Example of method overloading:**

```swift
class Shape {
    func draw() {
        print("Drawing a shape")
    }
}

class Circle: Shape {
    override func draw() {
        print("Drawing a circle")
    }
}

class Square: Shape {
    override func draw() {
        print("Drawing a square")
    }
}

let shape: Shape = Circle()
shape.draw() // prints "Drawing a circle"

let shape: Shape = Square()
shape.draw() // prints "Drawing a square"
```

> In this example, the draw() method is overloaded in the Circle and Square classes. When we call the draw() method on a Shape object, the compiler will automatically call the correct draw() method based on the type of the object.
> 

### **Example of method overriding:**

The following code shows an example of method overriding:

```swift
class Animal {
    func makeSound() {
        print("Animal sound")
    }
}

class Dog: Animal {
    override func makeSound() {
        print("Woof!")
    }
}

class Cat: Animal {
    override func makeSound() {
        print("Meow!")
    }
}

let animal: Animal = Dog()
animal.makeSound() // prints "Woof!"

let animal: Animal = Cat()
animal.makeSound() // prints "Meow!"
```

> In this example, the makeSound() method is overridden in the Dog and Cat classes. When we call the makeSound() method on an Animal object, the compiler will automatically call the correct makeSound() method based on the type of the object.
> 

### **Benefits of polymorphism:**

- Flexibility: Polymorphism makes code more flexible by allowing you to write code that can be used with different types of objects. This allows you to develop more reusable and adaptable software.
- Extensibility: Polymorphism makes code more extensible by allowing you to add new functionality to existing classes without having to modify the existing code. This makes it easier to maintain and update your software over time.
- Reduced complexity: Polymorphism can help to reduce the complexity of your code by allowing you to write more general-purpose functions and classes. This can make your code easier to understand and maintain.

## **Is a relationship vs has a relationship:**

### **Is-a relationship:**

The is-a relationship indicates that one class is a subclass of another class. This means that the subclass inherits all of the properties and behaviors of the superclass, plus any additional properties and behaviors that are specific to the subclass.

Examples:

- A dog is-an animal.This means that a dog inherits all of the properties and behaviors of an animal, such as having four legs, a tail, and the ability to make sound.
- A car is-a vehicle.This means that a car inherits all of the properties and behaviors of a vehicle, such as having wheels, an engine, and the ability to move.

### **Has-a relationship:**

The has-a relationship indicates that one object contains or references another object.

Examples:

- A dog has-a tail.This means that a dog has a physical part called a tail.
- A car has-a steering wheel.This means that a car contains a physical object called a steering wheel.

### **How to know if a relationship is is-a or has-a:**

To know if a relationship is is-a or has-a, you can ask yourself the following question:

- Can the subclass exist without the superclass?
- Can the object exist without the object it contains or references?

If the answer is no to both questions, then the relationship is is-a.

If the answer is yes to either question, then the relationship is has-a.

Example:

```swift
class Animal {
    var name: String

    init(name: String) {
        self.name = name
    }
}

class Dog: Animal {
    var breed: String

    init(name: String, breed: String) {
        super.init(name: name)
        self.breed = breed
    }
}

class Car {
    var steeringWheel: SteeringWheel

    init(steeringWheel: SteeringWheel) {
        self.steeringWheel = steeringWheel
    }
}
```

> In this example, the Dog class is-an Animal. This means that a Dog cannot exist without an Animal.
> 
> 
> *However, the `Car` class has-a `SteeringWheel`. This means that a `Car` can exist without a `SteeringWheel`.*
> 

### **When to use is-a vs has-a?**

You should use the is-a relationship when modeling real-world relationships between different types of objects. For example, a `Dog` is-an `Animal` and a `Car` is-a `Vehicle`.

You should use the has-a relationship when modeling relationships between objects where one object contains or references another object. For example, a `Car` has-a `SteeringWheel` and a `Dog` has-a `Tail`.

## **4- Abstraction:**

Abstraction is the process of hiding the underlying implementation details of something and exposing only the essential information that is needed to use it. This can make things easier to understand, use, and maintain.

Imagine a car. When you drive a car, you don’t need to know how the engine works or how the transmission works. You just need to know how to steer, accelerate, and brake. The car abstracts away all of the underlying complexity and makes it easy to use.

Another real-life example of abstraction is a smartphone. When you use your smartphone, you don’t need to know how the processor works or how the operating system works. You just need to know how to tap on the screen, type on the keyboard, and speak into the microphone. The smartphone abstracts away all of the underlying complexity and makes it easy to use.

### **How to use abstraction:**

There are many different ways to use abstraction but some common techniques include:

- Classes: Classes and structs are a powerful way to abstract away the underlying implementation details of your code. You can use classes to create objects that represent real-world entities, such as cars, smartphones, and bank accounts.

```swift
// Class representing a car
class Car {
    private var make: String
    private var model: String
    private var year: Int

    init(make: String, model: String, year: Int) {
        self.make = make
        self.model = model
        self.year = year
    }

    // Getter method for the make property
    func getMake() -> String {
        return make
    }

    // Setter method for the make property
    func setMake(newMake: String) {
        make = newMake
    }

    // ... other getter and setter methods for the model and year properties

    // Method to drive the car
    func drive() {
        print("Driving the car...")
    }
}
```

> In this example, the Car class abstract away the underlying implementation details of cars respectively. The user of the code does not need to know how the car works internally in order to use it. They can simply use the getter and setter methods to access and modify the properties of the car and use the methods to drive the car.
> 
- Protocols: Protocols are another way to abstract away the underlying implementation details of your code. Protocols allow you to define the behavior of a type without specifying how that behavior is implemented. This can make your code more flexible and reusable.

```swift
// Protocol representing a vehicle
protocol Vehicle {
    func drive()
}

// Class representing a car that conforms to the Vehicle protocol
class Car: Vehicle {
    func drive() {
        print("Driving the car...")
    }
}

// Class representing a truck that conforms to the Vehicle protocol
class Truck: Vehicle {
    func drive() {
        print("Driving the truck...")
    }
}

// Function that takes a Vehicle as a parameter and drives it
func driveVehicle(vehicle: Vehicle) {
    vehicle.drive()
}

// Usage:

let car = Car()
let truck = Truck()

// Drive the car and the truck
driveVehicle(vehicle: car)
driveVehicle(vehicle: truck)
```

> In this example, the Vehicle protocol defines the behavior of a vehicle without specifying how that behavior is implemented. The Car class and the Truck class both conform to the Vehicle protocol, and they each provide their own implementation of the drive() method.
> 
> 
> *The `driveVehicle()` function takes a `Vehicle` as a parameter and drives it. The function does not need to know what type of vehicle it is driving, as long as the vehicle conforms to the `Vehicle` protocol.*
> 
> *This makes the `driveVehicle()` function more flexible and reusable. It can be used to drive any type of vehicle, as long as the vehicle conforms to the `Vehicle` protocol.*
> 

### **Benefits of using abstraction:**

- Reduced complexity: Abstraction can help to reduce the complexity of your code by hiding away the underlying implementation details. This can make your code easier to understand, use, and maintain.
- Increased flexibility: Abstraction can make your code more flexible by allowing you to change the underlying implementation details without affecting the users of your code.
- Improved reusability: Abstraction can make your code more reusable by allowing you to create libraries and frameworks that can be used by other developers without them needing to know the underlying implementation details.

## **Finally:**

OOP is a powerful tool that can be used to develop a wide variety of software applications. By understanding the basic concepts of OOP, you can write more modular, maintainable, reusable, and flexible code.

**OOP** stands for **Object-Oriented Programming**. It’s a programming paradigm (or style) based on the concept of **"objects"** — these objects can contain **data** (called attributes or properties) and **functions** (called methods) that operate on the data.

---

###  Key Concepts of OOP:

1. **Class**:
    
    A blueprint for creating objects. Think of it like a template.
    
2. **Object**:
    
    An instance of a class. For example, if `Car` is a class, then `myCar` is an object of that class.
    
3. **Encapsulation**:
    
    Hides the internal state of the object and only exposes necessary parts. You control access using things like `public`, `private`, `protected`.
    
4. **Inheritance**:
    
    Allows one class to inherit the properties and methods of another. Helps in code reuse. (e.g., `Dog` inherits from `Animal`).
    
5. **Polymorphism**:
    
    Means "many forms." You can use a single function or method name to do different things based on the context (e.g., function overriding or overloading).
    
6. **Abstraction**:
    
    Hiding complex implementation details and showing only the essential features to the user.

   ---
   ---
