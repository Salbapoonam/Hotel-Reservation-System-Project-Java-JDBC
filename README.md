<h1>Hotel Reservation System</h1>

This project is a simple **Hotel Reservation System** built in Java using JDBC and MySQL. It provides functionalities for managing reservations, viewing reservation details, updating records, and deleting reservations from a MySQL database.

## Features

1. **Reserve a Room**: Add new reservations by providing guest name, room number, and contact information.
2. **View Reservations**: Display all current reservations in a formatted table.
3. **Get Room Number**: Retrieve the room number of a specific reservation by reservation ID and guest name.
4. **Update Reservations**: Modify existing reservations, including guest name, room number, and contact details.
5. **Delete Reservations**: Remove reservations using their reservation ID.
6. **Exit System**: Gracefully exit the program.

## Prerequisites

To run this project, ensure you have the following installed:

- Java Development Kit (JDK) 8 or later
- MySQL Server
- MySQL Connector/J (JDBC Driver)
- IDE or text editor for Java (e.g., IntelliJ IDEA, Eclipse, or VS Code)

## Database Setup

1. Create a MySQL database named `hotel_db`.
2. Use the following SQL script to create the `reservations` table:

```sql
CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY, -- Unique reservation ID
    guest_name VARCHAR(100) NOT NULL,             -- Guest's name
    room_number INT NOT NULL,                     -- Room number
    contact_number VARCHAR(15),                   -- Guest's contact number
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP -- Date of reservation
);
```

3. Insert sample data (optional):

```sql
INSERT INTO reservations (guest_name, room_number, contact_number)
VALUES ('John Doe', 101, '1234567890'),
       ('Jane Smith', 102, '0987654321');
```

## Configuration

Update the following constants in the `HotelReservationSystem` class with your MySQL credentials:

```java
private static final String url = "jdbc:mysql://localhost:3306/hotel_db";
private static final String username = "root";
private static final String password = "your_password";
```

## Running the Project

1. Clone this repository:

```bash
git clone https://github.com/your_username/hotel-reservation-system.git
cd hotel-reservation-system
```

2. Compile and run the program using your preferred IDE or terminal:

```bash
javac HotelReservationSystem.java
java HotelReservationSystem
```

## Usage

1. When the program starts, you will see the following menu:

```
HOTEL MANAGEMENT SYSTEM
1. Reserve a room
2. View Reservations
3. Get Room Number
4. Update Reservations
5. Delete Reservations
0. Exit
Choose an option:
```

2. Select an option by entering the corresponding number.
3. Follow the prompts to perform the desired action.

## Example Output

**View Reservations:**

```
Current Reservations:
+----------------+-----------------+---------------+----------------------+-------------------------+
| Reservation ID | Guest           | Room Number   | Contact Number      | Reservation Date        |
+----------------+-----------------+---------------+----------------------+-------------------------+
| 1              | John Doe        | 101           | 1234567890          | 2025-01-07 10:15:30    |
| 2              | Jane Smith      | 102           | 0987654321          | 2025-01-07 11:20:45    |
+----------------+-----------------+---------------+----------------------+-------------------------+
```


Thank you for using the **Hotel Reservation System**!

