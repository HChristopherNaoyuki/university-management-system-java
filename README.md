# University Personnel Management System

A simple Java application demonstrating object-oriented programming principles 
through a university personnel hierarchy. The system models various roles using 
inheritance and encapsulation.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Class Hierarchy (UML)](#class-hierarchy-uml)
- [Installation](#installation)
- [Usage](#usage)
- [Disclaimer](#disclaimer)

## Overview

This project implements a basic **University Management System** in Java. 
It represents the personnel structure of a university using the following classes:

- `Person` – abstract base class
- `Student` – inherits from `Person`
- `Employee` – inherits from `Person`
- `Faculty` – inherits from `Employee`
- `Staff` – inherits from `Employee`
- `MyDate` – utility class for handling dates

The design demonstrates key OOP concepts including **inheritance**, **polymorphism**, **encapsulation**, and proper method overriding.

## Features

- Common attributes and behavior defined in the `Person` base class
- Specialized student information (class standing)
- Employee details (office, salary, hire date)
- Faculty-specific attributes (office hours, academic rank)
- Staff-specific attribute (job title)
- Clean `toString()` implementations for readable output
- Simple console-based demonstration via `TestProgram`

## Class Hierarchy (UML)

```
+--------------------------+
|        Person            |
+--------------------------+
| - name: String           |
| - address: String        |
| - phoneNumber: String    |
| - emailAddress: String   |
+--------------------------+
| + toString(): String     |
+--------------------------+
           ▲
           │
   ┌───────┴────────┐
   │                │
+----------------+  +-----------------------+
|    Student     |  |      Employee         |
+----------------+  +-----------------------+
| - classStatus  |  | - office: String      |
|   : String     |  | - salary: double      |
+----------------+  | - dateHired: MyDate   |
| + toString()   |  +-----------------------+
+----------------+  | + toString(): String  |
                    +-----------------------+
                             ▲
                ┌────────────┴────────────┐
                │                         │
      +------------------+     +-------------------+
      |     Faculty      |     |      Staff        |
      +------------------+     +-------------------+
      | - officeHours    |     | - title: String   |
      |   : String       |     +-------------------+
      | - rank: String   |     | + toString()      |
      +------------------+     +-------------------+
      | + toString()     |
      +------------------+
```

## Installation

1. Clone the repository

   ```bash
   git clone https://github.com/HChristopherNaoyuki/university-management-system-java.git
   ```

2. Navigate to the project directory

   ```bash
   cd university-management-system-java
   ```

3. Compile all Java source files

   ```bash
   javac *.java
   ```

4. Run the demonstration program

   ```bash
   java TestProgram
   ```

**Note:** Make sure you are using Java 8 or higher.

## Usage

The included `TestProgram` class creates sample instances of:

- Student
- Faculty
- Staff

and prints their details using the overridden `toString()` methods.

Example output includes name, address, contact information, status/rank/title, salary (if applicable), office location, hire date, etc.

You can extend the test class or create your own main program to experiment with additional objects and behavior.

## Disclaimer

DISCLAIMER  

UNDER NO CIRCUMSTANCES SHOULD IMAGES OR EMOJIS BE INCLUDED DIRECTLY IN THE README FILE. 
ALL VISUAL MEDIA, INCLUDING SCREENSHOTS AND IMAGES OF THE APPLICATION, MUST BE STORED IN 
A DEDICATED FOLDER WITHIN THE PROJECT DIRECTORY. THIS FOLDER SHOULD BE CLEARLY STRUCTURED 
AND NAMED ACCORDINGLY TO INDICATE THAT IT CONTAINS ALL VISUAL CONTENT RELATED TO THE 
APPLICATION (FOR EXAMPLE, A FOLDER NAMED images, screenshots, or media).  

I AM NOT LIABLE OR RESPONSIBLE FOR ANY MALFUNCTIONS, DEFECTS, OR ISSUES THAT MAY OCCUR AS 
A RESULT OF COPYING, MODIFYING, OR USING THIS SOFTWARE. IF YOU ENCOUNTER ANY PROBLEMS OR 
ERRORS, PLEASE DO NOT ATTEMPT TO FIX THEM SILENTLY OR OUTSIDE THE PROJECT. INSTEAD, KINDLY 
SUBMIT A PULL REQUEST OR OPEN AN ISSUE ON THE CORRESPONDING GITHUB REPOSITORY, SO THAT IT 
CAN BE ADDRESSED APPROPRIATELY BY THE MAINTAINERS OR CONTRIBUTORS.

---
