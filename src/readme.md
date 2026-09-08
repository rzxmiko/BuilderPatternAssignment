# Java Builder Pattern - Car Manufacturing Demo

A simple Java project demonstrating the Builder design pattern. It builds different car types (`CityCar` and `SportsCar`) using method chaining, default values, and input validation.

## Project Structure

* `Car.java` - The main Product class with private fields and `printInfo()` method.
* `CarBuilder.java` - Interface that defines the builder step-by-step methods (Fluent API).
* `CityCarBuilder.java` - Builder for city cars. Sets default values for Honda City and checks that speed does not exceed 200 km/h.
* `SportsCarBuilder.java` - Builder for sports cars. Sets default values for Porsche 911 and checks that speed is at least 200 km/h.
* `Main.java` - Client code demonstrating standard creation, customization, and error handling.

## Rules & Features

* **Fluent Interface:** Allows chaining methods together like `.setColor("Blue").setMaxSpeed(160).build()`.
* **Default Values:** If you don't pass parameters, the builders use pre-configured defaults so objects aren't created with `null` fields.
* **Validation:** Calling `.build()` validates constraints and throws `IllegalArgumentException` if speed limits are broken.

## How to Run

Compile and run the `Main` class using your IDE or from terminal:

```bash
javac com/aitu/carbuilder/*.java
java com.aitu.carbuilder.Main