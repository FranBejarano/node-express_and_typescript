# Node + Express with TypeScript

Node + Express with TypeScript is a simple web application that provides a RESTful API for managing todo items. This project demonstrates how to set up a basic Express.js server using TypeScript and handle routes for managing todo items.

## Table of Contents

- [Node + Express with TypeScript](#node--express-with-typescript)
  - [Table of Contents](#table-of-contents)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Routes](#routes)
  - [Error Handling](#error-handling)
  - [Contributing](#contributing)
  - [License](#license)

## Installation

To get started with this project, follow these steps:

1. **Clone the Repository:** Clone this repository to your local machine using Git:

   ```bash
   git clone https://github.com/FranBejarano/node-express_and_typescript.git
   ```

2. **Navigate to the Project Directory:** Use the `cd` command to enter the project directory:

   ```bash
   cd node-express-typescript
   ```

3. **Install Dependencies:** Install the required dependencies using npm or yarn:

   ```bash
   npm install
   ```

   or

   ```bash
   yarn install
   ```

## Usage

Once you have installed the project, you can run it using the following command:

```bash
npm start
```

This will start the Express server on port 3000 by default. You can access the API at `http://localhost:3000`.

## Routes

This project provides the following routes for managing todo items:

- `GET /todos`: Get a list of all todo items.
- `POST /todos`: Create a new todo item.
- `GET /todos/:id`: Get a specific todo item by ID.
- `PUT /todos/:id`: Update a specific todo item by ID.
- `DELETE /todos/:id`: Delete a specific todo item by ID.

You can interact with these routes using tools like Postman or by making HTTP requests from your frontend application.

## Error Handling

The project includes basic error handling. If an error occurs, it will return a 500 Internal Server Error response with a JSON message. The error handler middleware is defined as follows:

```typescript
app.use((err: Error, req: Request, res: Response, next: NextFunction) => { 
    res.status(500).json({ message: err.message });
});
```

Please note that this error handling is minimal and is provided for demonstration purposes. In a production application, you would want to implement more robust error handling and logging.

## Contributing

Contributions to this project are welcome! If you would like to contribute:

1. Fork the repository.

2. Create a new branch for your feature or bug fix:

   ```bash
   git checkout -b feature-name
   ```

3. Make your changes and commit them with a clear and concise message:

   ```bash
   git commit -m "Add feature or fix bug"
   ```

4. Push your changes to your fork:

   ```bash
   git push origin feature-name
   ```

5. Create a pull request to the `main` branch of the original repository.

6. Your pull request will be reviewed, and once approved, it will be merged.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
