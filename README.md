# 📝 ToDo-APP-main (Backend API)

This repository contains the backend API for a simple To-Do Application. It is built using **Node.js, Express, and Mongoose**, following a standard structure for a RESTful API.

---

## ✨ Features

* **RESTful API:** Provides endpoints for creating, reading, updating, and deleting (CRUD) To-Do items.
* **Database Integration:** Uses **MongoDB** for data persistence via the Mongoose ODM.
* **Configuration:** Secure handling of environment variables using `dotenv`.
* **Development Ready:** Includes `nodemon` for automatic server restarts during development.

---

## 🛠️ Technology Stack

* **Runtime:** Node.js
* [cite_start]**Framework:** Express.js [cite: 1]
* **Database:** MongoDB
* [cite_start]**ODM:** Mongoose [cite: 1]
* [cite_start]**Environment Variables:** `dotenv` [cite: 1]
* [cite_start]**Development Utility:** `nodemon` [cite: 1]

---

## 🚀 Setup and Installation

Follow these steps to get the development environment running on your local machine.

### Prerequisites

* Node.js (LTS version recommended)
* MongoDB Instance (Local or Cloud service like MongoDB Atlas)

### Steps

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/ToDo-APP-main.git](https://github.com/YourUsername/ToDo-APP-main.git)
    cd ToDo-APP-main
    ```

2.  **Install Dependencies:**
    [cite_start]Install all required packages listed in `package.json`[cite: 1]:
    ```bash
    npm install
    ```

3.  **Create Environment File:**
    [cite_start]Create a file named `.env` in the root directory [cite: 1] and add your configuration details:

    *`.env` Example:*
    ```
    PORT=4000
    MONGODB_URL="mongodb://localhost:27017/todo-db" 
    ```

4.  **Start the Server:**

    * **Development Mode (with Nodemon):**
        ```bash
        npm run dev 
        ```
        [cite_start]The server will automatically restart when changes are made to `index.js` or other watched files[cite: 1]. The console will log: `server started at [PORT]`.

    * **Production/Test Mode:**
        ```bash
        npm start
        ```
        *(Note: The current `test` script in `package.json` runs `node index.js` which is used here as a standard start command for simplicity)*

The server will be running on the port specified in your `.env` file (e.g., `http://localhost:4000`).

---

## 🔌 API Endpoints

The API is mounted under the `/api/v1` route.

| HTTP Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/api/v1/todos` | Retrieve all To-Do items. |
| `GET` | `/api/v1/todos/:id` | Retrieve a single To-Do item by ID. |
| `POST` | `/api/v1/todos` | Create a new To-Do item. |
| `PUT` | `/api/v1/todos/:id` | Update an existing To-Do item. |
| `DELETE` | `/api/v1/todos/:id` | Delete a To-Do item. |
| `GET` | `/` | Simple homepage test (responds with `<h1> this is homepage</h1>`). |

---

## 🔑 Configuration

The primary configuration is managed in the `.env` file, which is ignored by Git for security.

| Variable | Description | Default/Example |
| :--- | :--- | :--- |
| `PORT` | The port the server will run on. | `4000` |
| `MONGODB_URL` | The connection string for the MongoDB database. | `mongodb://localhost:27017/todo-db` |

---

## 📄 Scripts

[cite_start]The following scripts are available in the `package.json`[cite: 1]:

* `npm run test`: Executes `node index.js`.
* `npm run dev`: Executes `nodemon index.js` for development with automatic restarts.

---

## 🔒 Security Note

The `.gitignore` file includes entries to prevent sensitive files from being committed:
* `/node_modules`
* `/.env`

---

## 🧑‍💻 Author

[Pratiik-glitch]

---
