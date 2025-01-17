# Roxiler Systems MERN Stack Coding Challenge

---


A **full-stack MERN application** built to manage and analyze product transactions using data fetched from a third-party API. This project demonstrates the integration of **MongoDB**, **Express.js**, **React**, and **Node.js** to create an efficient and interactive solution to manage product transactions.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [API Endpoints](#api-endpoints)
  - [Initialize Database](#initialize-database)
  - [List Transactions](#list-transactions)
  - [Statistics](#statistics)
  - [Bar Chart Data](#bar-chart-data)
  - [Pie Chart Data](#pie-chart-data)
  - [Combined Data](#combined-data)
- [Frontend Features](#frontend-features)
- [How to Run the Project](#how-to-run-the-project)


## Project Overview
This project is a coding challenge for **Roxiler Systems**, where the goal was to:
1. Create a backend API using the **MERN stack** to handle product transaction data.
2. Use a third-party API to seed the database.
3. Develop a frontend interface that allows users to view transactions, view statistics, and visualize data through bar and pie charts.

The backend provides multiple APIs to fetch and process transaction data, while the frontend is a single-page application that integrates with the backend APIs to display the transaction table, statistics, and charts.

## Features
### Backend:
- Fetches and stores product transaction data from a third-party API.
- APIs to:
  - Initialize the database with product transaction data.
  - List all product transactions with search and pagination support.
  - Retrieve statistics about sales (total sale amount, sold and unsold items).
  - Provide data for bar and pie charts based on the selected month.
  - Combine responses from multiple endpoints into a single response.
  
### Frontend:
- Transaction table that displays the product transactions for the selected month.
- Search functionality for transactions by title, description, or price.
- Pagination for browsing through transaction records.
- Displays sales statistics for the selected month.
- Bar chart showing price ranges and item counts.
- Pie chart showing item distribution across categories.

## Technologies Used
- **Frontend:**
  - React.js
  - Axios (for HTTP requests)
  - React Charts (for data visualization)
  - React Router (for client-side routing)

- **Backend:**
  - Node.js
  - Express.js
  - MongoDB (Database)
  - Mongoose (for MongoDB ODM)
  - Axios (for fetching third-party API data)

- **Dev Tools:**
  - Webpack (for bundling)
  - Babel (for transpiling)
  - npm (Node Package Manager)

## Installation

### Prerequisites
To run this project, ensure you have the following installed:
- **Node.js**: [Download Node.js](https://nodejs.org/)
- **MongoDB**: A local or cloud instance of MongoDB (e.g., MongoDB Atlas).

### Steps to Run the Project Locally:

1. **Clone the repository**:

    ```bash
    git clone https://github.com/AnkitSingh9496/Roxiler-MERN-Challenge.git
    cd Roxiler-Systems-Assignment-main
    ```
2. **Install dependencies**:

   - For the backend:
     ```bash
     cd backend
     npm install
     ```

   - For the frontend:
     ```bash
     cd frontend
     npm install
     ```

3. **Setup Environment Variables**:
   - Create a `.env` file in the `backend` directory to configure your MongoDB URI and other environment variables:
   
     ```text
     MONGO_URI=mongodb://localhost:27017/your-database-name
     PORT=5000
     ```

4. **Start the Backend**:
   From the `backend` directory, run the following command to start the server:

   ```bash
   npm run dev
   ```

5. **Start the Frontend**:
   From the `frontend` directory, run the following command to start the React application:

   ```bash
   npm start
   ```

6. **Access the Application**:
   Open your browser and go to `http://localhost:3000` to view the frontend. The backend should be running on `http://localhost:5000`.

## API Endpoints

### Initialize Database
- **URL**: `/api/initialize`
- **Method**: `GET`
- **Description**: Fetches product transaction data from the third-party API and initializes the database with the data.
- **Response**: Initializes MongoDB with product transaction data.

### List Transactions
- **URL**: `/api/transactions`
- **Method**: `GET`
- **Query Parameters**:
  - `month`: The month for which to retrieve the transactions (e.g., `January`).
  - `search`: Optional text to filter transactions by title, description, or price.
  - `page`: Page number for pagination (default: `1`).
  - `perPage`: Number of transactions per page (default: `10`).
  
- **Response**: A paginated list of transactions for the selected month.

### Statistics
- **URL**: `/api/statistics`
- **Method**: `GET`
- **Query Parameters**:
  - `month`: The month for which to retrieve the statistics (e.g., `January`).
  
- **Response**:
  - `totalSaleAmount`: The total sales amount for the selected month.
  - `totalSoldItems`: The total number of sold items.
  - `totalUnsoldItems`: The total number of unsold items.

### Bar Chart Data
- **URL**: `/api/bar-chart`
- **Method**: `GET`
- **Query Parameters**:
  - `month`: The month for which to retrieve bar chart data (e.g., `January`).
  
- **Response**:
  - Price ranges and item counts for the selected month.

### Pie Chart Data
- **URL**: `/api/pie-chart`
- **Method**: `GET`
- **Query Parameters**:
  - `month`: The month for which to retrieve pie chart data (e.g., `January`).
  
- **Response**:
  - Categories and item counts for the selected month.

### Combined Data
- **URL**: `/api/combined-data`
- **Method**: `GET`
- **Query Parameters**:
  - `month`: The month for which to retrieve combined data (e.g., `January`).
  
- **Response**: A combined response containing transactions, statistics, bar chart data, and pie chart data.

## Frontend Features

- **Transaction Table**:
  - Displays transactions of the selected month.
  - Provides search and pagination functionality.
  - Updates dynamically based on user input.

- **Transaction Statistics**:
  - Displays total sale amount, number of sold items, and unsold items for the selected month.

- **Bar Chart**:
  - Displays a bar chart with price ranges and item counts for the selected month.

- **Pie Chart**:
  - Displays a pie chart with the distribution of items across categories for the selected month.


---

