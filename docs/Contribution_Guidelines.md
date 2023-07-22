# Contribution Guidelines

Thank you for your interest in contributing to the Sara project! We welcome contributions from the community to help improve and enhance the functionality of our AI-powered executive assistant. To ensure a smooth and collaborative development process, we have established the following contribution guidelines.

## Git Branching Model

We follow the Git branching model known as GitFlow. This model provides a clear structure for managing feature development, bug fixes, and releases. The main branches in our repository are:

- `main`: The main branch contains the stable and production-ready code. It should always reflect the latest release.
- `develop`: The develop branch is the main branch for ongoing development. Feature branches are created from and merged back into this branch.
- `feature/*`: Feature branches are created for developing new features or enhancements. They are based on the `develop` branch and merged back into it when the feature is complete.
- `bugfix/*`: Bugfix branches are created for fixing bugs or issues. They are based on the `develop` branch and merged back into it when the bug is resolved.
- `release/*`: Release branches are created for preparing a new release. They are based on the `develop` branch and merged into both `develop` and `main` branches when the release is ready.

## Code Reviews

All contributions to the Sara project must go through a code review process. This ensures that the code meets our quality standards and maintains consistency throughout the project. To initiate a code review, follow these steps:

1. Create a new branch based on the appropriate branch for your contribution (e.g., `feature/*` or `bugfix/*`).
2. Implement your changes and commit them to your branch.
3. Push your branch to the remote repository.
4. Create a pull request (PR) on GitHub, targeting the appropriate branch (`develop` for features and bug fixes, `main` for releases).
5. Assign the PR to a reviewer, who will review the code and provide feedback.
6. Address the feedback and make any necessary changes.
7. Once the reviewer approves the changes, the PR can be merged into the target branch.

## Coding Standards

To maintain a consistent codebase, we follow a set of coding standards. Please adhere to the following guidelines when contributing to the Sara project:

- Use meaningful variable and function names that accurately describe their purpose.
- Write clear and concise comments to explain the code's functionality and any complex logic.
- Follow the Python style guide (PEP 8) for code formatting and indentation.
- Use type hints to provide clear and explicit information about function parameters and return values.
- Avoid unnecessary code duplication by reusing existing functions and modules.
- Write unit tests for new features and ensure that existing tests pass before submitting a contribution.

## License

By contributing to the Sara project, you agree that your contributions will be licensed under the project's open-source license. Please review the license information provided in the `README.md` file for more details.

We appreciate your interest in contributing to Sara and look forward to your valuable contributions!