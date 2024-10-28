# 🍽️ Digital Menu API

A simple Java-based REST API for managing digital menus, built with **Spring Boot** and **PostgreSQL**. This API offers basic functionality to handle GET and POST requests. It is my first API built in Java after working primarily as a JavaScript fullstack developer.

## 🌟 Features
- **Get Menu Items**: Retrieve all available menu items.
- **Add Menu Items**: Add new items to the digital menu.
- **Database Integration**: Fully integrated with **PostgreSQL** for persistent data storage.

---

## 🛠️ Tech Stack

- **Java** 21
- **Spring Boot** 3.3.5
- **PostgreSQL** for database
- **Maven** for dependency management
- **Lombok** for reducing boilerplate code

---

## ⚙️ Installation and Setup

### Prerequisites
- **Java 21** or higher
- **PostgreSQL** installed and running
- **Maven** installed

### Clone the Repository
First, clone the repository to your local machine:
```bash
git clone https://github.com/yourusername/digital-menu-api.git
cd digital-menu-api
```

### Database Setup
1. Create a PostgreSQL database:
   ```sql
   CREATE DATABASE digital_menu;
   ```
2. Update your `application.properties` file (or `application.yml`) with your PostgreSQL credentials:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/digital_menu
   spring.datasource.username=yourUsername
   spring.datasource.password=yourPassword
   ```

### Build and Run the Project
Use Maven to install dependencies and run the application:
```bash
mvn clean install
mvn spring-boot:run
```

The server should now be running at `http://localhost:8080`.

---

## 🛠️ Usage

### API Endpoints

#### Get Menu Items
- **Endpoint**: `GET /menu/items`
- **Description**: Retrieves all the items from the menu.

```bash
curl -X GET http://localhost:8080/menu/items
```

#### Add Menu Item
- **Endpoint**: `POST /menu/items`
- **Description**: Add a new item to the menu.
- **Request Body** (JSON):
  ```json
  {
    "name": "Pasta Carbonara",
    "description": "Classic Italian pasta with creamy sauce.",
    "price": 12.99
  }
  ```

Example usage:
```bash
curl -X POST http://localhost:8080/menu/items -H "Content-Type: application/json" -d '{"name":"Pasta Carbonara", "description":"Classic Italian pasta with creamy sauce", "price":12.99}'
```

---

## 🧰 Dependencies

The following dependencies are included in the `pom.xml`:

- **Spring Boot Starter Web**: To build RESTful APIs.
- **Spring Boot Starter Data JPA**: For easy database integration.
- **PostgreSQL**: PostgreSQL driver to connect to the database.
- **Lombok**: Reduces boilerplate Java code.
- **Spring Boot DevTools**: Hot-reloading during development.
- **Spring Boot Starter Test**: For writing tests.

---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Here's how to contribute:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add a new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

---

## 📧 Contact

If you have any questions or feedback, feel free to reach out:

- **GitHub**: [@love-quinn](https://github.com/love-quinn)
- **Website**: https://love-quinn.github.io/
