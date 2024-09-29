---
title: Development
has_children: false
nav_order: 5
---

# Development

## DVCS
To track the development of our project, I used a Github repository and created a dedicated organization called `unibo-dtm-se-2324-graphProject`. The main repository is `Artifact.`, the repository follows a straightforward branching strategy with a single main branch, which contains the stable release of the project. All changes, including new features and bug fixes, are committed directly to this branch.

Commits were written following the [Conventional Commit](https://www.conventionalcommits.org/en/v1.0.0/) approach. A commit is therefore written in the following format:

```bash
<type>[optional scope]: <description>
```

The types of commits that have been adopted in my case are as follows:

- **chore**: for changes that do not affect the production code;
- **refactor**: for changes to the code that do not relate to either bug fixes or the addition of a new feature (e.g., moving a method from one class to another);
- **fix**: Corrections for identified bugs or any other problem noticed in the code.

## Implementation details

- Throughout the development process, several key lessons were learned, and noteworthy implementations were made:

**Interactive Graph Plotting**: A key feature developed is the ability to create and manipulate one or two graphs simultaneously. This enhances the user experience by allowing for comparative analysis, which is particularly beneficial for students learning mathematical concepts.

**Responsive Design**: The application emphasizes creating a responsive user interface that adapts to various screen sizes, ensuring accessibility for all users, whether they are accessing the application on a desktop, tablet, or mobile device.

**Event-Driven Architecture**: The application employs an event-driven approach for user interactions. By leveraging event listeners for button clicks and form submissions, the application maintains a clean separation of concerns, making the codebase more maintainable.

**Linting for Code Quality**: ESLint was integrated into the development workflow, ensuring code quality and adherence to best practices. This helps in maintaining a clean and efficient codebase throughout the project's lifecycle.

**Continuous Integration**: A GitHub Actions workflow was established to automate testing and deployment processes. This ensures that every commit is automatically tested, providing immediate feedback on code quality and functionality.
