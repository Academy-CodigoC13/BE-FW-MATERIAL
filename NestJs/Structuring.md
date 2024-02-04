# Structuring Nestjs Projects: Best Practices and Example

 NestJS is a framework for building scalable and maintainable server-side applications using TypeScript. The structure might vary based on the specific requirements of your project, but a well-organized project structure is crucial for building robust and maintainable applications. In this guide, we’ll explore the best practices for structuring NestJS projects.

 Usually, NestJS architecture is based on the following features:
 - Controllers
 - Modules
 - Services

 All the above features are organized in a modular way. This means that a module in NestJS serves as a container for organizing and encapsulating different parts of your application


![alt text](image-1.png)

## Explanation:

- **src**: This is the main source code directory.
    - **app**: The main module of your application.
        - **controllers**: Controllers handle incoming requests and return responses.
        - **modules**: Different modules of your application. Each module can have its **controllers**, services, and other components.
        - **services**: Business logic and data manipulation are handled by services.
    - **config**: Configuration files for your application.
    - **dto**: Data Transfer Objects (DTOs) for defining the structure of data passed between different layers of your application.
    - **middleware**: Custom middleware for processing requests before they reach the controllers.
    - **entities**: Database entities or data models for interacting with databases.
    - **filters**: Custom exception filters for handling exceptions globally.
    - **guards**: Authorization guards for controlling access to routes.
    - **interceptors**: Interceptors can be used to modify the request/response objects globally.
    - **pipes**: Pipes are used to transform the data coming into the application.
- **main.ts**: The entry point of your application where you bootstrap NestJS.

- **app.controller.spec.ts, app.service.spec.ts, etc.**: Unit test files for your controllers, services, and other components.

- **README.md**: Documentation for your project.

- **tsconfig.json**: TypeScript configuration file.

- **package.json**: Node.js package file with dependencies and scripts.