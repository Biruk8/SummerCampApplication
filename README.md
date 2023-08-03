# Simple Web Application with Express and MongoDB

This is a simple web application built with Express and MongoDB, allowing users to process applications, review applications, select applicants based on GPA, and remove all applications.

## Prerequisites

Before running the application, make sure you have the following installed:

- Node.js
- MongoDB
- npm (Node Package Manager)

## Installation

1. Clone the repository to your local machine.
2. Navigate to the project directory using the terminal or command prompt.
3. Install the required dependencies by running:

```bash
npm install
```

## Configuration

Create a `.env` file in the root directory and add the following environment variables:

```
MONGO_DB_USERNAME=your_mongodb_username
MONGO_DB_PASSWORD=your_mongodb_password
MONGO_DB_NAME=your_mongodb_database_name
MONGO_COLLECTION=your_mongodb_collection_name
```

Replace `your_mongodb_username`, `your_mongodb_password`, `your_mongodb_database_name`, and `your_mongodb_collection_name` with your MongoDB credentials.

## Usage

1. Start the application by running:

```bash
npm start
```

2. The server will be running at http://localhost:port/ where `port` is the port number specified during startup.

3. Access the application in your web browser using the URLs mentioned below:

- Home Page: http://localhost:port/
- Apply Page: http://localhost:port/apply
- Review Application Page: http://localhost:port/review-application
- Select Applicants by GPA Page: http://localhost:port/select-by-gpa
- Remove All Applications Page: http://localhost:port/remove-all-applications

## Endpoints

1. **Process Application (POST):** `/processApplication`
   - This endpoint allows users to submit their application with their name, email, GPA, and background. The application data will be stored in the MongoDB database.

2. **Review Application (POST):** `/reviewApplication`
   - Users can review an application by providing the applicant's email. The application data associated with the provided email will be fetched from the MongoDB database and displayed.

3. **Select Applicants by GPA (POST):** `/SelectbyGpa`
   - Users can select applicants based on a minimum GPA provided as input. The server will retrieve all applicants from the database and display those with a GPA greater than or equal to the input GPA.

4. **Remove All Applications (POST):** `/RemovedAdmin`
   - This endpoint is used to remove all applications from the MongoDB database.

## Additional Notes

- The project uses the `ejs` templating engine for rendering views.
- Ensure that you have MongoDB running and accessible before starting the server.
- The application should be used for learning purposes and may require additional security measures and error handling for production use.

## Contributors

This project was developed by Biruk8.

Feel free to contribute or provide feedback to improve this simple web application.

**Enjoy Coding!**
