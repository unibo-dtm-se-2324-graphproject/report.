---
title: Release
has_children: false
nav_order: 7
---

# Release

The Graph Website is released and distributed through the npm (Node Package Manager) registry, which serves as the primary platform for sharing JavaScript packages and libraries. This choice allows for seamless installation and integration into various development environments, enhancing accessibility for users.

**Release Process**

- Versioning: Each release follows the Semantic Versioning (SemVer) principles, ensuring that users are informed of the nature of changes made. The versioning scheme allows users to understand whether updates include breaking changes (MAJOR), new features (MINOR), or bug fixes (PATCH).

- Publishing to npm: The project is published to the npm registry using the command
  npm publish --access public
  This command uploads the latest version of the project, along with its dependencies and metadata, making it available for public access.

- Continuous Integration/Continuous Deployment (CI/CD): The project utilizes GitHub Actions to automate the publishing process. Each time code is merged into the main branch, the CI/CD pipeline automatically runs tests, builds the project, and publishes it to npm if all checks pass. This ensures that the most stable and tested version of the application is available to users.

**Accessing the Project**

Users can install the Graph Website package directly from the npm registry using the following command:

npm install imane01-graph

This command will download the latest version of the Graph Website package.

## Choice of the license

The Graph Project is licensed under the MIT License. This choice was made to encourage open collaboration and allow users to freely utilize, modify, and distribute the software. The MIT License is well-regarded in the open-source community for its simplicity and permissiveness, making it an ideal choice for educational tools that aim to reach a broad audience, including students and educators.

### Human Explanation

| Permissions | Limitations | Conditions |
| ------------ |------------ |------------ |
✅ Commercial use | ❌ Liability  | ℹ License and copyright notice |
✅ Modification | ❌ Warranty | |
✅ Distribution |  |  |
✅ Private use |  |  |

## Choice of the versioning schema

Choice of the Versioning Schema

For versioning the Graph Project, I utilize Semantic Versioning (SemVer), which follows the format MAJOR.MINOR.PATCH:

- MAJOR version increments signify breaking changes that might disrupt existing functionality. For example, if a future version alters how users interact with the graphing features, the MAJOR version will be incremented.
- MINOR version increments indicate the addition of new features in a manner that is backward-compatible. An example would be the introduction of a new graph type that does not affect existing functionality.
- PATCH version increments are used for backward-compatible bug fixes. These updates address issues reported by users without changing the overall user experience or existing features.

In particular, I used the following approach:

**MAJOR** release
* No current commits indicate a breaking change that would require a major version bump.

**MINOR** release
* Commit type fix:
    * Incrementing the version number for publishing indicates new features or improvements (e.g., fix(package): increment version number for publishing).
* Commit type chore with scope api-deps:
    * Updates to dependencies or improvements that enhance existing features (e.g., fix(package): update package name and dependencies).

**PATCH** release
* Commit type fix:
    * Corrections for identified bugs or issues, as seen in multiple commits such as fix(workflow): set registry-url for npm publish and fix(lint): add missing globals package to resolve linting errors.
* Commit type refactor:
    * Refactoring of existing code to improve structure or efficiency without altering functionality (e.g., refactor(script): remove unused 'e' variable to resolve ESLint linting errors).

**No release**
* Commit types such as test, build, and general maintenance commits that do not meet the criteria for a version increase.
