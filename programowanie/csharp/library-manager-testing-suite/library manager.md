# Library Manager System Documentation

## 1. Project Overview

This document defines the requirements and structure for the **Library Manager System** project.

The project is intended as an introductory application written in **C#**. The implementation should remain relatively simple so that the main emphasis can be placed on **writing automated tests**. The application is expected to support basic library operations such as managing books, managing patrons, and handling borrowing and returning of books.

A persistent data store shall be used instead of in-memory collections. The project should therefore introduce basic database integration while keeping the business rules straightforward and suitable for a beginner-level implementation.

---

## 2. Project Goals

The project should aim to achieve the following objectives:

- implement a simple C# application with clear domain logic,
- use a database for storing application data,
- separate business logic from data access concerns,
- create a comprehensive automated test suite,
- apply the **Arrange-Act-Assert (AAA)** testing pattern consistently.

The primary educational focus shall be placed on **test design and test coverage**, rather than on advanced architectural complexity.

---

## 3. Suggested Solution Structure

The solution should be divided into at least the following projects:

1. **LibraryManager.Core**  
   Contains domain models, interfaces, and business logic.

2. **LibraryManager.Infrastructure**  
   Contains database access logic, persistence configuration, and repository implementations.

3. **LibraryManager.Tests**  
   Contains automated tests for the business logic, written using **NUnit**.

Additional projects may be introduced if necessary, but the overall structure should remain simple and easy to understand.

---

## 4. Technology Requirements

The project should be implemented using the following technologies:

- **C#**
- **.NET**
- **NUnit** for testing
- **A relational database** for persistent storage
- **Entity Framework Core** is recommended for database access, as it is beginner-friendly and widely used

A lightweight database engine such as **SQLite** is recommended for simplicity, although another relational database may also be used.

---

## 5. Functional Scope

The application shall support the following operations:

- adding books,
- registering patrons,
- borrowing books,
- returning books,
- viewing stored books and patrons.

The business logic should remain limited to essential validation and status changes.

---

## 6. Data Model

The following entities shall be implemented.

### 6.1. Book

Represents a book available in the library.

#### Properties

- `Id` (`int` or `Guid`) - unique identifier
- `Title` (`string`) - title of the book
- `Author` (`string`) - author of the book
- `IsAvailable` (`bool`) - indicates whether the book is currently available for borrowing; default value should be `true`

### 6.2. Patron

Represents a library user.

#### Properties

- `Id` (`int` or `Guid`) - unique identifier
- `Name` (`string`) - full name of the patron

### 6.3. BorrowRecord

A separate entity to store borrowing history.

#### Suggested Properties

- `Id` (`int` or `Guid`) - unique identifier
- `BookId` - identifier of the borrowed book
- `PatronId` - identifier of the patron
- `BorrowDate` (`DateTime`) - date of borrowing
- `ReturnDate` (`DateTime?`) - date of return, if returned

This entity is optional for a beginner implementation. If omitted, the borrowing state may be represented only through the `IsAvailable` property in the `Book` entity.

---

## 7. Database Requirements

The application shall use a database to store all data persistently.

### 7.1. Persistence

The following data shall be stored in the database:

- books,
- patrons,
- borrowing information.

### 7.2. Database Access

Database communication should be abstracted from the main business logic. This may be achieved through:

- a `DbContext` if Entity Framework Core is used,
- repositories or service classes for reading and writing data.

The implementation should remain simple and readable. Excessive abstraction is not required for this project.

### 7.3. Database Constraints

The following basic rules should be enforced either in code or through database configuration:

- a book must have a title,
- a book must have an author,
- a patron must have a name,
- a borrowed book must not be borrowed again until it is returned.

---

## 8. Business Logic

A service class such as `LibraryService` shall be implemented to handle core operations.

### 8.1. Required Methods

The service should implement at least the following methods.

#### `void AddBook(Book book)`

Adds a new book to the system.

**Validation requirements:**
- `ArgumentNullException` shall be thrown if `book` is `null`.

#### `void RegisterPatron(Patron patron)`

Registers a new patron.

**Validation requirements:**
- `ArgumentNullException` shall be thrown if `patron` is `null`.

#### `void BorrowBook(int bookId, int patronId)`

Marks a book as borrowed by a patron.

**Validation requirements:**
- `ArgumentException` shall be thrown if the specified book does not exist.
- `ArgumentException` shall be thrown if the specified patron does not exist.
- `InvalidOperationException` shall be thrown if the book is already borrowed.

#### `void ReturnBook(int bookId)`

Marks a borrowed book as returned.

**Validation requirements:**
- `ArgumentException` shall be thrown if the specified book does not exist.
- `InvalidOperationException` shall be thrown if the book is already available.

### 8.2. Optional Read Methods

The following methods may also be added to simplify testing and application usage:

- `IEnumerable<Book> GetAllBooks()`
- `IEnumerable<Patron> GetAllPatrons()`
- `Book? GetBookById(int bookId)`
- `Patron? GetPatronById(int patronId)`

These methods are not mandatory, but they are useful for verification and presentation purposes.

---

## 9. Testing Requirements

The testing part of the project is the main priority. The `LibraryManager.Tests` project shall verify the behavior of the application logic thoroughly.

### 9.1. Testing Framework

All tests shall be written using **NUnit**.

The use of additional assertion libraries is optional, but standard NUnit assertions are sufficient for this project.

### 9.2. Testing Pattern

All tests shall follow the **Arrange-Act-Assert (AAA)** pattern.

The structure of each test should clearly reflect the following phases:

- **Arrange** - prepare the test data, dependencies, and initial state,
- **Act** - execute the method being tested,
- **Assert** - verify the result.

This pattern shall be applied consistently throughout the test suite.

### 9.3. Scope of Testing

Tests should focus primarily on the business logic implemented in `LibraryService`.

If database-related logic is separated properly, unit tests may target the service layer while integration tests may be added for persistence behavior. For a beginner-level project, it is acceptable to focus mostly on service tests, provided that the database usage is still covered at least at a basic level.

---

## 10. Required Test Scenarios

At minimum, the following test cases shall be implemented.

### 10.1. Book Management Tests

1. Adding a valid book should increase the total number of stored books.
2. Adding a `null` book should throw `ArgumentNullException`.

### 10.2. Patron Management Tests

1. Registering a valid patron should increase the total number of stored patrons.
2. Registering a `null` patron should throw `ArgumentNullException`.

### 10.3. Borrowing Tests

1. Borrowing an existing available book by an existing patron should change the book status to unavailable.
2. Attempting to borrow a book that does not exist should throw `ArgumentException`.
3. Attempting to borrow a book for a patron that does not exist should throw `ArgumentException`.
4. Attempting to borrow a book that is already borrowed should throw `InvalidOperationException`.

### 10.4. Returning Tests

1. Returning a borrowed book should change the book status to available.
2. Attempting to return a book that does not exist should throw `ArgumentException`.
3. Attempting to return a book that is already available should throw `InvalidOperationException`.

---

## 11. Test Quality Expectations

The test suite should meet the following quality expectations:

- each test should verify one behavior,
- test names should clearly describe the expected result,
- tests should be independent from one another,
- test data should be easy to read and maintain,
- AAA structure should be clearly visible in every test.

If comments are used, they may explicitly label the `Arrange`, `Act`, and `Assert` sections, although this is not strictly required if the structure is already obvious.

---

## 12. Non-Functional Requirements

The project should also satisfy the following non-functional requirements:

- code should be readable and beginner-friendly,
- naming should follow standard C# conventions,
- classes and methods should have clear responsibilities,
- the database layer should be simple and understandable,
- the solution should compile and tests should execute successfully.

The implementation should avoid unnecessary complexity. The purpose of the project is to practice clean coding and testing fundamentals, not advanced enterprise patterns.

---

## 13. Acceptance Criteria

The project shall be considered complete when all of the following conditions are met:

1. The application is implemented in **C#**.
2. The application uses a **database** for persistent storage.
3. The required entities and service methods are implemented.
4. Automated tests are written using **NUnit**.
5. The **Arrange-Act-Assert** pattern is consistently applied in tests.
6. All required test scenarios described in this document are covered.
7. The solution compiles successfully and all implemented tests pass.
8. The code remains simple enough for a beginner to understand and extend.

---

## 14. Summary

The **Library Manager System** should be implemented as a simple C# project with database support and a strong emphasis on testing. The application logic should remain uncomplicated, while the test suite should be treated as the central part of the exercise. The use of **NUnit** and the **AAA** pattern is required, and the final solution should demonstrate clear separation of concerns, correct validation behavior, and reliable automated verification.