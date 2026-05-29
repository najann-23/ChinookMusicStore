# Chinook Music Store Management System

## Overview
The Chinook Music Store Management System is a Java-based desktop application built using Swing and MySQL (Chinook sample database).  
It was developed as the final project for the Object-Oriented Programming course (ITE23005) at The Saigon International University.

The system manages a digital music store including artists, albums, tracks, customers, invoices, and revenue analytics.



## Key Features
- Full CRUD operations for Artist, Album, Track, Customer, Invoice
- User authentication with BCrypt password hashing
- Role-based access control (Admin / Viewer)
- Search, filter, and sort across all tables
- Dashboard with KPI statistics
- Data visualization with JFreeChart:
  - Top Artists (Bar Chart)
  - Revenue by Genre (Pie Chart)
- Excel export feature using Apache POI
- Background processing using SwingWorker for smooth UI



## Technologies Used
- Java 11+
- Java Swing (GUI)
- MySQL (Chinook Database)
- JDBC
- Maven
- JFreeChart
- Apache POI
- BCrypt
- JUnit 5


## Architecture
The project follows MVC architecture with DAO layer:

- **Model**: Entity classes (Artist, Album, Track, Customer, Invoice, User, etc.)
- **View**: Swing UI (Login, Dashboard, CRUD panels)
- **Controller**: Handles user interaction and logic
- **DAO**: Database access layer using JDBC + PreparedStatement
- **Util**: Utilities (DB connection, security, export, charts)

### Design Patterns
- Singleton → DatabaseConnection  
- Observer → Chart auto-refresh  
- Strategy → Sorting system  
- Factory → DAO creation  



## Database (Chinook)
Based on the open-source Chinook database (MySQL version).

Main tables:
- Artist
- Album
- Track
- Customer
- Invoice
- InvoiceLine
- Playlist
- Genre
- MediaType
- Users (custom authentication table)



## How to Run
1. Import project into Eclipse  
2. Configure MySQL and import Chinook database  
3. Update DB credentials in `DatabaseConnection`  
4. Run `Main.java`  
5. Login with Admin or Viewer account  

---

## Roles
| Role   | Permissions |
|--------|------------|
| Admin  | Full CRUD + export + dashboard |
| Viewer | Read-only access |

---

## Testing
- JUnit 5 unit tests for DAO and utilities
- In-memory H2 database for testing
- JaCoCo coverage report (>70%)

---

## Export Feature
- Export table data to `.xlsx`
- Implemented using Apache POI
- Supports formatted headers + summary rows

---

## Author
Lê Nguyễn Quỳnh Trang  
Saigon International University  
Object-Oriented Programming (ITE23005)

---

## Notes
This project demonstrates:
- Object-Oriented Programming principles
- MVC + DAO architecture
- JDBC database integration
- Modern Java features (Stream API, Optional, records)
- Real-world software design practices
