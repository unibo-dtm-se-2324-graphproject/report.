---
title: Development
has_children: false
nav_order: 5
---

# Development

## DVCS
To track the development of my project, I used a Github repository and created a dedicated organization called `unibo-dtm-se-2324-graphproject`. The main repository is `graphproject`, the repository follows a straightforward branching strategy with a single main branch, which contains the stable release of the project. All changes, including new features and bug fixes, are committed directly to this branch.

Commits were written following the [Conventional Commit](https://www.conventionalcommits.org/en/v1.0.0/) approach. A commit is therefore written in the following format:

```bash
<type>[optional scope]: <description>
```

The types of commits that have been adopted in my case are as follows:

- **chore**: for changes that do not affect the production code;
- **refactor**: for changes to the code that do not relate to either bug fixes or the addition of a new feature 
- **fix**: Corrections for identified bugs or any other problem noticed in the code.

Example of commit messages:

- **chore(package)**: add placeholder build script to prevent CI failure
- **refactor(server)**: update server setup for testing compatibility
- **fix(package)**: rename the package to a unique name for publishing

**Frequency and Granularity**

- Atomic Commits: Changes to the Graph Website project are committed regularly in small, focused increments, which simplifies tracking the project's development and allows for easy reversion if necessary.

- Granularity: Each commit corresponds to a specific logical update, such as adding, fixing bugs in the code, or enhancing the user interface, ensuring that modifications are clearly defined and manageable.

## Implementation details

**Libraries**

- *math.js: A powerful library for parsing and evaluating mathematical expressions, enabling dynamic calculations of user-defined equations within the application.

- Plotly: An interactive graphing library that allows for the creation of dynamic and visually appealing plots.

**API**

The Graph Project utilizes an API built with Express.js, designed for handling user requests related to mathematical graph generation and visualization. This API facilitates communication between the front end and the back end, managing input data from users, such as equations and graph parameters. 

Tools and Platforms 

- Express.js: A minimal and flexible web application framework that provides robust features for building APIs. It simplifies routing and middleware integration, making it easier to manage server responses and user requests.

- Visual Studio Code:
An integrated development environment (IDE) that provides essential tools for coding, debugging, and version control. It enhances productivity with features like syntax highlighting and extensions tailored for JavaScript development.

- Git and GitHub:
Version control systems are used for tracking changes in the project’s codebase and facilitating collaboration. GitHub serves as a remote repository for code storage, issue tracking, and project management.

- npm:
The package manager for JavaScript manages project dependencies and facilitates the installation of libraries, such as math.js and Plotly, essential for the functionality of the application.

**Programming Languages:**

1. JavaScript: The primary language used for both the backend (Node.js) and frontend components of the Graph Project.
2. HTML: Used for structuring the web pages and content in the front end of the application.
3. CSS: Employed for styling the frontend components, enhancing the visual appearance and user experience of the web application.

**Dependencies**

- Express: ^4.21.0 is a dependency in my project because it serves as the foundation for my server-side application, handling routing and requests efficiently. It enables me to build a robust API for my graph visualization system, ensuring seamless communication between the frontend and backend.


**DevDependencies:**

- eslint: For linting JavaScript code to ensure code quality.
- eslint-plugin-react: A plugin for ESLint to lint React code.
- globals: Provides global variable definitions for various environments.
- jest: A testing framework for running unit tests.
- supertest: A library for testing HTTP servers in Node.js.

- Throughout the development process, several key lessons were learned and I am personally proud of:

**Interactive Graph Plotting**: A key feature developed is the ability to create and manipulate one or two graphs simultaneously. This enhances the user experience by allowing for comparative analysis, which is particularly beneficial for students learning mathematical concepts.

**Responsive Design**: The application emphasizes creating a responsive user interface that adapts to various screen sizes, ensuring accessibility for all users, whether they are accessing the application on a desktop, tablet, or mobile device.

**Event-Driven Architecture**: The application employs an event-driven approach for user interactions. By leveraging event listeners for button clicks and form submissions, the application maintains a clean separation of concerns, making the codebase more maintainable.

**Linting for Code Quality**: ESLint was integrated into the development workflow, ensuring code quality and adherence to best practices. This helps in maintaining a clean and efficient codebase throughout the project's lifecycle.

**Continuous Integration**: A GitHub Actions workflow was established to automate testing and deployment processes. This ensures that every commit is automatically tested, providing immediate feedback on code quality and functionality.





