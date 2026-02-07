# Contributing to ShelbyNet Client

First off, thank you for taking the time to contribute! It’s developers like you who make the ShelbyNet ecosystem faster and more robust.

## 🛠️ How Can I Contribute?

### Reporting Bugs
* Check the **Issues** tab to see if the bug has already been reported.
* If not, open a new issue. Use a clear title and provide a minimal reproduction case.
* Include your environment details (Node version, OS, Aptos network used).

### Suggesting Enhancements
* Open an issue with the tag `enhancement`.
* Explain the use case and how it benefits the ShelbyNet community.

### Pull Requests
1. **Fork** the repository and create your branch from `main`.
2. **Install dependencies**: `pnpm install`.
3. **Lint & Test**: Ensure your code passes existing linting rules and include new tests for new features.
4. **Link Issues**: Reference any related issues in your PR description.
5. **Sign-off**: Ensure your commits are signed (GPG) if required by the maintainers.

## 📜 Coding Standards
* We follow the **Prettier** and **ESLint** configurations defined in the repo.
* Use descriptive variable names and provide JSDoc comments for public functions.
* Keep Aptos Move interactions modular to allow for future protocol upgrades.

## 🏗️ Development Setup
1. Clone your fork.
2. Create a local `.env` file based on `.env.example`.
3. Run `pnpm dev` to start the local development server.