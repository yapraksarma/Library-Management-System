# Library Management System

A Java-based library management system that handles books and magazines with different borrowing rules, priorities, and member types.

## Features

- Item management (Books and Magazines)
- Member hierarchy with different discount levels
  - General Members (0% discount)
  - Students without Scholarship (20% discount)
  - Students with Scholarship (30% discount)
- Priority-based pricing
  - Noteworthy
  - Highly Significant
  - Invaluable
- Late charge calculation
- Search functionality by title and type
- Borrowing charge calculation with member discounts

## Project Structure

### Core Classes

- **BorrowedItem**: Abstract base class for all borrowable items
- **Book**: Extends BorrowedItem with book-specific attributes
- **Magazine**: Extends BorrowedItem with magazine-specific attributes

### Member Classes

- **Member**: Abstract base class for all member types
- **General**: Regular members with no discount
- **StudentWScholar**: Students with scholarship (30% discount)
- **StudentWoScholar**: Students without scholarship (20% discount)

### Interfaces

- **Borrowable**: Defines methods for charge calculations
- **Searchable**: Defines search functionality

## Business Rules

### Books
- Daily Price: $5
- Penalty Day: 10 days
- Late Charge: $5 if borrowed time exceeds penalty days

### Magazines
- Daily Price: $10
- Penalty Day: 7 days
- Late Charge: $2 if borrowed time exceeds penalty days

### Pricing Formula
Total Charge = (Daily Price × Days × Priority) - Discount + Late Charge
