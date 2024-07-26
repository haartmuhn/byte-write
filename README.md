<div align="center">

# Byte Write

[![License: MIT](https://img.shields.io/badge/License-MIT-darkgreen.svg)](https://opensource.org/licenses/MIT)
![CSS3 Badge](https://img.shields.io/badge/css-1572B6?logo=css3&logoColor=fff&style=flat)
![JavaScript Badge](https://img.shields.io/badge/js-F7DF1E?logo=javascript&logoColor=000&style=flat)
![JSON Badge](https://img.shields.io/badge/json-FF0000?logo=json&logoColor=fff&style=flat)
![npm Badge](https://img.shields.io/badge/npm-A020F0?logo=npm&logoColor=fff&style=flat)
![Node.JS Badge](https://img.shields.io/badge/node-orange?logo=node.js&logoColor=fff&style=flat)

</div>

Byte Write is a blog site built using Handlebars.js, Sequelize, and Express.js. This application follows the MVC paradigm and is configured to work with a PostgreSQL database. It supports user authentication and CRUD operations for posts and comments.


## Description

This project is a blog platform that allows users to create, edit, delete, and view blog posts and comments. Users can also manage their accounts and authenticate securely. The application uses Handlebars.js for templating, Sequelize for ORM, and Express.js for routing and server management.

## Table of Contents

- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [Tests](#tests)
- [License](#license)

## Installation

1.  Clone the repository:

```bash
git clone https://github.com/haartmuhn/byte-write.git
cd byte-write
```

2.  Install the dependencies:

```
npm install
```

3.  Set Up Environmental Variables:

- Create a `.env` file based on `.env.example`
- Update the `.env` file with your database credentials and session secret.

4.  Set up your PostgreSQL database:

- Create a database with the name specified in your `.env` file (`DB_NAME`).

5.  Run migrations to set up the database schema:

```bash
npx sequelize-cli db:migrate

```

6.  Start the application:

 ```bash
 node server.js
 ```

 7. Open your web browser and navigate to `http://localhost:3001` to view the application.

 Note: The following adjustments were made to the project files to enable deployment to RENDER:

 -  **server.js**
    -   Ensured the session secret is fetched from environment variables.
    -   Configured the `express.static` to use `path.join` for serving static files.

-   **config/connection.js**
    -   Updated to use `DATABASE_URL` environment variable for the PostgreSQL connection.
    -   Enabled SSL connection for PostgreSQL.

-   **.env**
    -   Added `DATABASE_URL` for the PostgreSQL connection string.
    -   Added `SESSION_SECRET` for the session secret.


## Usage

-   **User Authentication**: Secure login and registration.
-   **CRUD Operations**: Create, read, update, and delete posts and comments.
-   **Responsive Design**: Mobile-friendly interface.
-   **Session Management**: User sessions managed using express-session.

<div align="center">

[Visit my website](https://byte-write.onrender.com/)

</div>

## Features

-   User authentication (signup, login, logout).
-   Session management with automatic timeout.
-   Create, read, update, and delete (CRUD) operations for blog posts.
-   Commenting system on blog posts.
-   Responsive design for mobile and desktop browsers.

## Contributing

Contributions to Byte Write are welcome! Here’s how you can contribute:

1. **Fork the repository** on GitHub.
2. **Create a branch** for your feature `git checkout -b new-feature`.
3. **Make changes** and commit them `git commit -m "Add some feature"`.
4. **Push to the branch** `git push origin new-feature`.
5. **Create a new Pull Request** against the main.

Please ensure your code adheres to the existing style of the project to make your changes easy to understand and integrate!

## Tests

To run tests, execute the following command:

```
npm test
```

(Note: You will need to write the tests based on the endpoints and operations your application performs, as this is not set up by default.)

## License

Byte Write is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute this application according to the terms of the license.