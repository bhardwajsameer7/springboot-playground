# Spring Boot Annotations Overview

| **Annotation**             | **Description**                                                                                                                                                                       |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `@SpringBootApplication`   | Main entry point for Spring Boot applications. Combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan` for configuring application context and starting the app. |
| `@ConfigurationProperties` | Binds external properties from `.properties` or `.yml` files to a Java object. Allows grouping configurations under a prefix, improving organization and type safety.                |
| `@RestController`          | Combines `@Controller` and `@ResponseBody` to handle REST requests and responses in a single class. It simplifies creating RESTful web services in Spring Boot.                     |
| `@Value`                   | Injects a single property from configuration files directly into fields or method parameters in your classes. Useful for quick property access.                                     |
| `@Component`               | Marks a Java class as a Spring-managed component. Used as a generic stereotype for any Spring-managed object, and picked up by component scanning.                                  |
| `@Service`                 | Specializes `@Component` for service layer components, indicating a class that holds business logic. Often used for service classes in the application layer.                       |
| `@Repository`              | Specializes `@Component` for the repository layer. Helps in exception translation, making it suitable for DAO classes that access the database.                                     |
| `@Autowired`               | Enables automatic dependency injection by type. Spring injects the required beans into fields, constructors, or methods with this annotation.                                       |
| `@Bean`                    | Defines a bean to be managed by the Spring container. Used in configuration classes to manually instantiate, configure, and manage beans.                                           |
| `@Entity`                  | Marks a class as an entity to be mapped to a database table. Typically used in JPA-based applications to represent database entities.                                               |
| `@Table`                   | Specifies the table name associated with an entity class. Used with `@Entity` for custom table mappings.                                                                            |
| `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping` | Specialized annotations for handling HTTP GET, POST, PUT, and DELETE requests, respectively. These map requests to methods in `@RestController`. |
| `@RequestMapping`          | Maps HTTP requests to specific methods or classes. It can handle multiple HTTP methods (GET, POST, etc.) and is commonly used in controllers.                                     |
| `@PathVariable`            | Binds a method parameter to a URI template variable in the request URL. Helps retrieve dynamic segments of the URI.                                                                |
| `@RequestParam`            | Extracts query parameters from HTTP requests and binds them to method parameters in the controller.                                                                                |
| `@ExceptionHandler`        | Defines a method to handle exceptions in `@Controller` classes. Allows customizing the response when an error occurs in a specific handler.                                       |
| `@ControllerAdvice`        | A global error-handling mechanism for controllers. It allows defining `@ExceptionHandler` methods that apply across multiple controllers.                                         |
| `@EnableAutoConfiguration` | Allows Spring Boot to automatically configure components based on dependencies in the classpath. Included by default in `@SpringBootApplication`.                                |
| `@ConditionalOnProperty`   | Enables a Spring bean only when a specific property is set in the configuration. Useful for conditional bean loading based on external properties.                                 |
