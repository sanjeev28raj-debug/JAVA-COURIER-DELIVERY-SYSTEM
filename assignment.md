Java Courier Delivery System – Assignment

1. Title

Courier and Delivery System using Java

2. Aim

To develop a simple Java program to manage courier package details and demonstrate inheritance and method overriding using a fragile package example.

3. Objective

- To create a "Package" class.
- To store the tracking ID and package weight.
- To create a "FragilePackage" subclass.
- To add insurance value for fragile packages.
- To demonstrate inheritance using "extends".
- To demonstrate method overriding using "@Override".
- To use constructors for initializing object values.

4. Problem Statement

A courier company needs to maintain basic information about packages. Every package has a tracking ID and weight. A fragile package has an additional insurance value.

Design a Java program using Object-Oriented Programming concepts to represent these package details.

5. Concepts Used

Class

A class is a blueprint used to create objects.

Object

An object is an instance of a class. In this program, "p" is an object of "FragilePackage".

Inheritance

Inheritance allows one class to acquire the properties and methods of another class.

class FragilePackage extends Package

Here, "FragilePackage" inherits from "Package".

Constructor

A constructor initializes the values of an object.

Method Overriding

The "display()" method of the parent class is redefined in the "FragilePackage" class.

super()

The "super()" keyword is used to call the constructor of the parent class.

6. Algorithm

1. Start the program.
2. Create the "Package" class.
3. Declare "trackingId" and "weightKg".
4. Create a constructor to initialize these values.
5. Create the "display()" method.
6. Create the "FragilePackage" class by extending "Package".
7. Add the "insuranceValue" variable.
8. Create the "FragilePackage" constructor.
9. Use "super()" to initialize the parent class values.
10. Override the "display()" method.
11. Create a "FragilePackage" object in the "main()" method.
12. Call the "display()" method.
13. Display the package details.
14. Stop the program.

7. Source Code

class Package {
    String trackingId;
    double weightKg;

    Package(String trackingId, double weightKg) {
        this.trackingId = trackingId;
        this.weightKg = weightKg;
    }

    void display() {
        System.out.println("Tracking ID: " + trackingId);
        System.out.println("Weight: " + weightKg + " kg");
    }
}

class FragilePackage extends Package {
    double insuranceValue;

    FragilePackage(String trackingId, double weightKg, double insuranceValue) {
        super(trackingId, weightKg);
        this.insuranceValue = insuranceValue;
    }

    @Override
    void display() {
        System.out.println("Tracking ID: " + trackingId);
        System.out.println("Weight: " + weightKg + " kg");
        System.out.println("Insurance Value: Rs." + insuranceValue);
    }
}

public class CourierDemo {
    public static void main(String[] args) {

        FragilePackage p = new FragilePackage(
            "TRK12345", 5.5, 10000
        );

        p.display();
    }
}

8. Sample Output

Tracking ID: TRK12345
Weight: 5.5 kg
Insurance Value: Rs.10000.0

9. Explanation of the Program

The "Package" class contains two variables: "trackingId" and "weightKg".

The "FragilePackage" class inherits these variables and methods from the "Package" class. It also adds a new variable called "insuranceValue".

The "display()" method is overridden in "FragilePackage" to display the tracking ID, weight, and insurance value.

In the "main()" method, a "FragilePackage" object is created with:

- Tracking ID: "TRK12345"
- Weight: "5.5 kg"
- Insurance Value: "Rs.10000"

The "display()" method then prints these details.

10. Applications

This concept can be used in:

- Courier management systems
- Delivery tracking systems
- E-commerce applications
- Logistics management
- Package management software

11. Advantages

- Simple and easy to understand.
- Demonstrates real-world use of inheritance.
- Reduces code duplication through inheritance.
- Method overriding provides specific behavior for fragile packages.
- Easy to extend with additional package types.

12. Conclusion

The Java Courier Delivery System successfully demonstrates important Object-Oriented Programming concepts such as classes, objects, constructors, inheritance, "super()", and method overriding.

The program can be further extended to support different delivery methods, package types, delivery charges, and tracking features.
