# Inventory Management System Backend

---

- RENDER HOSTED so please assume delay around 1 to 2 minute for server to wakeup from sleep

---

This repository contains the backend code for an Inventory Management System. It's built using Node.js, Express.js, and MongoDB, providing RESTful API endpoints for managing inventory items and suppliers.

## Setup Instructions

1.  Clone the repository to your local machine:

    ```bash
    git clone <repository_url>
    ```

2.  Install dependencies:

    ```bash
    cd inventorymanagementOnlineBE
    npm install
    ```

3.  Set up environment variables:

    Create a `.env` file in the root directory and define the following variables:

    ```
    PORT=3001
    MONGO_DB_URL=<your_mongodb_connection_string>
    ```

4.  Start the server:

    ```bash
    npm run dev
    ```

5.  Nodemon is available for local hosting, so change them in package.json for only the dev part

        ```bash

    "scripts" : {
    "dev": "nodemon index.js"
    }

    ````
    Then can Start the server.

      ```bash
    npm run dev
    ````

## API Endpoints

### Inventory

- **GET /api/inventory**: Fetch all inventory items with filtering, sorting, and pagination.
- **GET /api/inventory/:id**: Get information for a specific inventory item by ID.
- **POST /api/inventory**: Add a new inventory item.
- **DELETE /api/inventory/:id**: Delete an inventory item.
- **PUT /api/update-inventory/:id**: Update an inventory item or supplier.

### Data Management

- **POST /api/remove-all-data**: Remove all data from the database.
- **POST /api/populate-database**: Populate the database with at least 1000 rows of random data.

## Schemas

- **Inventory**: Represents an inventory item with properties such as item name, quantity, and supplier.
- **Supplier**: Represents a supplier with properties like name, address, and contact information.

## Dependencies

- **Express**: Web framework for Node.js.
- **Mongoose**: MongoDB object modeling tool.
- **Cors**: Middleware for enabling CORS (Cross-Origin Resource Sharing).
- **Dotenv**: Module for loading environment variables from a .env file.

## Contributing

Contributions are welcome! If you find any bugs or have suggestions for improvements, please open an issue or submit a pull request.
