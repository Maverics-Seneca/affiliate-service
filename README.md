# Affiliate Service

## Overview

The Affiliate Service is a key component of our healthcare microservices architecture, designed to manage pharmacy links and track clicks. Built with Node.js and Firebase Firestore, this service provides robust functionality for storing and managing affiliate links and tracking user interactions.

## Features

- Store and manage pharmacy affiliate links
- Track clicks on affiliate links
- Secure data storage using Firebase Firestore

## Tech Stack

- Node.js
- Express.js
- Firebase Firestore

## Project Structure

```
affiliate-service/
│── src/
│ ├── controllers/
│ │ ├── affiliateController.js
│ ├── routes/
│ │ ├── affiliateRoutes.js
│ ├── models/
│ │ ├── Affiliate.js
│ ├── config/
│ │ ├── firebase.js
│ ├── app.js
│── .github/workflows/
│── Dockerfile
│── package.json
│── README.md
```

## Setup and Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/Maverics-Seneca/affiliate-service.git
   ```

2. Install dependencies:
   ```sh
   cd affiliate-service
   npm install
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory and add the following:
   ```sh
   FIREBASE_PROJECT_ID=your_firebase_project_id
   FIREBASE_PRIVATE_KEY=your_firebase_private_key
   FIREBASE_CLIENT_EMAIL=your_firebase_client_email
   ```

4. Start the service:
   ```sh
   npm start
   ```

## API Endpoints

- `POST /affiliates` - Create a new affiliate link
- `GET /affiliates` - Retrieve all affiliate links
- `GET /affiliates/:id` - Retrieve a specific affiliate link
- `PUT /affiliates/:id` - Update an affiliate link
- `DELETE /affiliates/:id` - Delete an affiliate link
- `POST /affiliates/:id/click` - Record a click on an affiliate link

## Docker

To build and run the service using Docker:

```sh
docker build -t affiliate-service .
docker run -p 3000:3000 affiliate-service
```

## CI/CD

This project uses GitHub Actions for continuous integration and deployment. The workflow is defined in `.github/workflows/ci-cd.yml`.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
