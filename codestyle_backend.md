# Backend Codestyle for Contact Management System

This document outlines the coding standards and best practices for backend development using Spring Boot and related technologies.

## Basic Rules

- **Indentation**: Use 4 spaces for indentation.
- **Line Length**: No more than 100 characters per line.

## Naming Conventions

- **Classes**: Use PascalCase: `MyService`
- **Methods and Variables**: Use camelCase: `myMethod`
- **Constants**: Use ALL_CAPS with underscores: `MY_CONSTANT`

## Comments

- Use Javadoc-style comments for methods and classes.

## Formatting

- **Commas**: Place commas at the end of the line: `myList.add("item1"), "item2");`
- **Semicolons**: Use semicolons at the end of each statement.
- **Object Literals**: Add a space after the colon in key-value pairs: `Map<String, String> map = new HashMap<>();`

## General Principles

- Keep code simple, clean, and well-documented.
- Follow the DRY (Don't Repeat Yourself) principle.
- Use consistent naming conventions throughout the codebase.

## Package and Directory Structure

- Organize code into packages by feature or functionality.
- Keep a flat structure to avoid deep nesting of packages.

## Java

### Naming Conventions

- Use `CamelCase` for class names.
- Use `camelCase` for method names, local variables, and method parameters.
- Use `PascalCase` for enum constants.
- Use `UPPER_SNAKE_CASE` with leading underscores for private constants.

### Code Formatting

- Use 4 spaces for indentation.
- Keep lines within 120 characters for better readability.
- Place the opening brace `}` on the same line as the declaration for classes, methods, and constructors.

### Comments

- Use comments to explain the "why" behind the code, not the "what".
- Use Javadoc comments for public classes and methods to document APIs.

## REST API

### Routing

- Use `@RequestMapping` to define the base path for a controller.
- Use `@PostMapping`, `@GetMapping`, `@PutMapping`, `@DeleteMapping` for CRUD operations.

### Request and Response

- Use `@RequestBody` to receive JSON data in request body.
- Use `@PathVariable` to receive URL parameters.
- Use `@RequestParam` to receive query parameters.
- Return consistent response structures using a统一的响应实体，如 `Result` 类。

### Validation

- Validate incoming data and return meaningful error messages if validation fails.

### Pagination

- Support pagination in list APIs using query parameters like `pageNum` and `pageSize`.

## Database

### MyBatis Plus

- Use `LambdaQueryWrapper` for building type-safe queries.
- Use `Page` object for pagination.

### Transactions

- Use `@Transactional` annotation to manage transaction boundaries.

## Security

- Sanitize user inputs to prevent SQL injection and XSS attacks.
- Use HTTPS to secure data in transit.

## Logging

- Use a logging framework like SLF4J with Logback for logging.
- Use appropriate log levels (INFO, DEBUG, ERROR, etc.) for different types of log messages.

## Dependency Injection

- Use constructor injection for dependency injection.

## Code Linting and Formatting

- Use Checkstyle, PMD, or SpotBugs to enforce code quality rules.
- Use an IDE's auto-formatting feature to maintain consistent code formatting.

Adhere to these guidelines to maintain consistency and quality in your backend codebase. Adjust and extend this guide as needed based on project-specific requirements.