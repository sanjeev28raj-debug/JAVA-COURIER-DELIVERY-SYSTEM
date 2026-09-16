Java Courier Delivery System

📌 Project Description

This project is a simple Java-based Courier Delivery System developed to demonstrate important Object-Oriented Programming (OOP) concepts.

The program manages package details such as Tracking ID, Weight, and Insurance Value for fragile packages.

🎯 Objective

- To understand classes and objects in Java.
- To demonstrate inheritance.
- To demonstrate constructors.
- To demonstrate method overriding.
- To use "super()" to call the parent class constructor.

🛠️ Technologies Used

- Programming Language: Java
- Concepts: OOP, Inheritance, Constructor, Method Overriding

📂 Classes Used

1. Package

The "Package" class contains:

- "trackingId"
- "weightKg"
- Constructor to initialize package details
- "display()" method to display package information

2. FragilePackage

"FragilePackage" inherits from the "Package" class.

It additionally contains:

- "insuranceValue"

The "display()" method is overridden to display all package details.

3. CourierDemo

The "CourierDemo" class contains the "main()" method and creates an object of "FragilePackage".

💻 Program

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

▶️ Sample Output

Tracking ID: TRK12345
Weight: 5.5 kg
Insurance Value: Rs.10000.0

🔑 OOP Concepts Demonstrated

Concept| Usage
Class| "Package", "FragilePackage", "CourierDemo"
Object| "p"
Constructor| Initializes package details
Inheritance| "FragilePackage extends Package"
"super()"| Calls the parent constructor
Method Overriding| "display()" is redefined
Encapsulation| Package data is grouped with its methods

📖 Conclusion

This project successfully demonstrates how inheritance and method overriding can be used in a real-world courier delivery scenario using Java.

👨‍💻 Project Type

Academic / Java OOP Mini Project
