# Deployment using CI/CD GitHub Pipeline in Azure (Staging-Level / Production-level)

This project includes a CI/CD pipeline utilizing GitHub Actions for deployment on Azure at a staging level.

### CI/CD Pipeline Configuration

The CI/CD pipeline is defined in the `.github/workflows/main.yml` file. It performs the following actions:

- **Build and Test**: On each push to the repository, the pipeline triggers a build and runs tests to ensure code validity.

- **Deploy to Staging**: If the build and tests pass, the application is deployed to a staging environment on Azure.

### Azure Setup

1. Set up an Azure Web App for Node.js.

2. Configure the GitHub Actions workflow with Azure credentials and deployment details.

### How to Run Locally

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/your-repo.git
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Run the application:

    ```bash
    npm start
    ```

   The application will be accessible at [http://localhost:5000](http://localhost:5000).




## Node.js App with REST and GraphQL Example

This Node.js application demonstrates the usage of GraphQL queries and mutations along with a REST API using Node and Express.

## GraphQL Advantage

GraphQL allows clients to precisely define the data they need, reducing unnecessary data transfer over the network.

## Endpoints

- **REST API Endpoint**: [http://localhost:5000/rest/getAllUsers](http://localhost:5000/rest/getAllUsers)
- **GraphQL Endpoint**: [http://localhost:5000/graphql](http://localhost:5000/graphql)

## GraphQL Queries and Mutations

1. **Get All Users with Query Operation:**

    ```graphql
    query {
      getAllUsers {
        id
        email
      }
    }
    ```

2. **Get Single User Details:**

    ```graphql
    query {
      findUserById(id: 1000) {
        id
        firstName
        lastName
        email
      }
    }
    ```

3. **Create User with Mutation Operation:**

    ```graphql
    mutation {
      createUser(firstName: "sachin", lastName: "purohit", email: "sachin@sachin.com", password: "password") {
        id
        firstName
        lastName
        email
      }
    }
    ```

