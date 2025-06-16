# REST Assured Petstore

A Katalon Studio project demonstrating REST API testing using REST Assured library with the Swagger Petstore API.

## Overview

This project contains automated API tests for the Swagger Petstore API, showcasing various REST API testing scenarios including:

- Pet management (create, update, delete, find by status/tags)
- Store operations (inventory, orders)
- User management (create, update, delete, login/logout)

## Project Structure

```
├── Object Repository/Swagger Petstore/  # REST service objects
├── Scripts/                             # Test scripts
├── Test Cases/                          # Test case definitions
├── OpenAPI Specification/               # API specifications
├── Include/config/                      # Configuration files
└── Profiles/                           # Test execution profiles
```

## Technology Stack

- **Katalon Studio 10.2.x**: Test automation platform
- **REST Assured 3.3.0**: Java library for REST API testing
- **Groovy**: Scripting language for test implementation
- **Gradle**: Build automation

## Getting Started

### Prerequisites

- Katalon Studio 10.2.0 or later
- Java 8 or later
- Gradle (included via wrapper)

### Setup

1. Clone this repository
2. Run Gradle command to download dependencies:
   ```bash
   ./gradlew katalonCopyDependencies
   ```
3. Open the project in Katalon Studio

### Running Tests

#### Via Katalon Studio
1. Open the project in Katalon Studio
2. Navigate to Test Cases
3. Right-click on a test case and select "Run"

## API Endpoints Tested

The project tests the following Swagger Petstore API endpoints:

### Pet Operations
- `POST /pet` - Add a new pet
- `PUT /pet` - Update an existing pet  
- `GET /pet/findByStatus` - Find pets by status
- `GET /pet/findByTags` - Find pets by tags
- `GET /pet/{petId}` - Find pet by ID
- `POST /pet/{petId}` - Update pet with form data
- `DELETE /pet/{petId}` - Delete a pet
- `POST /pet/{petId}/uploadImage` - Upload pet image

### Store Operations
- `GET /store/inventory` - Get pet inventories by status
- `POST /store/order` - Place an order for a pet
- `GET /store/order/{orderId}` - Find purchase order by ID
- `DELETE /store/order/{orderId}` - Delete purchase order by ID

### User Operations
- `POST /user` - Create user
- `POST /user/createWithArray` - Create list of users with array input
- `POST /user/createWithList` - Create list of users with list input
- `GET /user/login` - Log user into the system
- `GET /user/logout` - Log out current logged in user session
- `GET /user/{username}` - Get user by username
- `PUT /user/{username}` - Update user
- `DELETE /user/{username}` - Delete user

## Configuration

### Build Configuration
The project uses Gradle with the Katalon plugin. Key dependencies are configured in `build.gradle` with explicit Groovy exclusions to avoid conflicts with Katalon's embedded Groovy version.

### Logging
Logging configuration is available in `Include/config/log.properties`.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests to ensure they pass
5. Submit a pull request

## License

This project is for demonstration purposes.