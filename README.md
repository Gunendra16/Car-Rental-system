# Car Rental System

## Overview

This Car Rental System is a console-based application developed using C++ and MySQL. The system allows users to view available cars, select a car to rent, and check the availability of each car. It connects to a MySQL database to store and retrieve car information, making it easy to manage car rentals and availability.

## Features

- **View Available Cars:** Users can view a list of all available cars along with their details such as brand, model, serial number, and rental price.
- **Select Car for Rent:** Users can select a car by entering its serial number. The system checks the availability of the car in the database and updates its status accordingly.
- **Real-time Database Interaction:** The application interacts with a MySQL database to fetch car details, check availability, and update the rental status in real-time.

## Requirements

- **C++ Compiler**: Ensure that a C++ compiler (like GCC or MSVC) is installed on your system.
- **MySQL Server**: A MySQL server must be running on your system. You can use tools like XAMPP, WAMP, or MySQL Workbench.
- **MySQL Connector/C++**: Install the MySQL Connector/C++ to enable database interaction from your C++ program.

## Setup Instructions

1. **Clone the Repository**
   ```sh
   git clone https://github.com/YourUsername/CarRentalSystem.git
   cd CarRentalSystem
   ```

2. **Configure MySQL Database**
   - Start your MySQL server.
   - Create a database named `mydb`.
   - Create a table `cars` with the following structure:
     ```sql
     CREATE TABLE cars (
         Serial INT PRIMARY KEY,
         Brand VARCHAR(50),
         Model VARCHAR(50),
         Rent INT,
         Avail BOOLEAN
     );
     ```
   - Insert initial data (optional):
     ```sql
     INSERT INTO cars (Serial, Brand, Model, Rent, Avail) VALUES 
     (123, 'Honda', 'Civic', 60, true),
     (223, 'Toyota', 'Yaris', 50, true),
     (323, 'Suzuki', 'Alto', 30, true);
     ```

3. **Update MySQL Credentials**
   - Open the `main.cpp` file and update the `HOST`, `USER`, `PW`, and `DB` constants with your MySQL server details.

4. **Compile and Run**
   - Compile the program using your C++ compiler.
   - Run the executable.

   ```sh
   g++ main.cpp -o CarRentalSystem -lmysqlclient
   ./CarRentalSystem
   ```

## Usage

1. **Start the Program:** Run the executable to start the Car Rental System.
2. **View Cars:** The system will display a list of all cars available for rent.
3. **Select a Car:** Enter the serial number of the car you want to rent. If available, the car will be booked for you.
4. **Exit:** Select the exit option to close the program.

## Contributing

Contributions are welcome! Please fork this repository and submit pull requests to add new features or fix issues.
