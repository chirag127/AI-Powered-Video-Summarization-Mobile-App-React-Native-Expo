# Contributing to VideoSum-AI-Video-Summarizer-Mobile-App

Thank you for your interest in contributing to VideoSum-AI-Video-Summarizer-Mobile-App! We welcome your contributions to help us improve this AI-powered mobile application.

## 1. Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to `chirag127@example.com`.

## 2. How to Contribute

We welcome contributions in the form of bug reports, feature requests, code improvements, and documentation updates.

### 2.1 Reporting Bugs

When reporting a bug, please provide as much detail as possible:

*   **Version:** The version of the app you are using.
*   **Device & OS:** Your device model and operating system version (e.g., iPhone 14 Pro, iOS 17.2; Samsung Galaxy S23, Android 14).
*   **Steps to Reproduce:** Clear, concise steps to reproduce the problem.
*   **Expected Behavior:** What you expected to happen.
*   **Actual Behavior:** What actually happened.
*   **Screenshots/Videos:** If applicable, attach screenshots or screen recordings.
*   **Logs:** Any relevant error messages or console logs.

Use the provided issue templates for bug reports.

### 2.2 Suggesting Enhancements

If you have an idea for a new feature or an improvement, please:

1.  **Check Existing Issues:** See if a similar feature request already exists.
2.  **Open a New Issue:** If not, create a new issue describing your suggestion. Be specific about the problem it solves and the proposed solution.

### 2.3 Contributing Code

We appreciate code contributions! Here's the general workflow:

1.  **Fork the Repository:** Create a fork of `https://github.com/chirag127/VideoSum-AI-Video-Summarizer-Mobile-App`.
2.  **Clone Your Fork:** Clone your forked repository to your local machine:
    bash
    git clone https://github.com/chirag127/VideoSum-AI-Video-Summarizer-Mobile-App.git
    cd VideoSum-AI-Video-Summarizer-Mobile-App
    
3.  **Set Up Development Environment:**
    *   Ensure you have Node.js and Expo CLI installed.
    *   Install dependencies:
        bash
        npm install
        
    *   Refer to the `README.md` for detailed setup instructions and available scripts.

4.  **Create a New Branch:** Create a descriptive branch for your changes:
    bash
    git checkout -b feat/your-feature-name
    # or
    git checkout -b fix/your-bug-fix
    

5.  **Make Your Changes:** Implement your feature or fix.

6.  **Test Your Changes:** Ensure all tests pass. Run the full test suite using:
    bash
    npm test
    
    For end-to-end tests, use:
    bash
    # Example for E2E testing (adjust command as per project setup)
    npx playwright test
    

7.  **Lint and Format:** Ensure your code adheres to the project's coding standards:
    bash
    npm run lint
    npm run format
    

8.  **Commit Your Changes:** Write clear and concise commit messages.
    bash
    git commit -m "feat: Add new summarization algorithm"
    # or
    git commit -m "fix: Resolve video playback issue on Android"
    

9.  **Push to Your Fork:** Push your branch to your fork:
    bash
    git push origin feat/your-feature-name
    

10. **Open a Pull Request:** Create a Pull Request from your branch to the `main` branch of the `chirag127/VideoSum-AI-Video-Summarizer-Mobile-App` repository.

    *   Provide a clear description of your changes.
    *   Reference any relevant issues.
    *   Ensure your PR passes all CI checks.

## 3. Project Standards & Guidelines

*   **Architecture:** We follow a Feature-Sliced Design (FSD) pattern where applicable for modularity. The core application logic should be separated from UI components and external services.
*   **TypeScript:** Use TypeScript with strict type checking (`strict: true` in `tsconfig.json`).
*   **React Native & Expo:** Leverage the Expo ecosystem for streamlined development and deployment.
*   **Testing:** Write comprehensive unit and integration tests using Vitest. End-to-end tests should be implemented using Playwright for cross-platform validation.
*   **Linting & Formatting:** Biome is used for linting and formatting to ensure code quality and consistency.
*   **AI Integration:** All interactions with AI models (e.g., summarization APIs) must be robust, handle potential errors gracefully, and follow security best practices.
*   **Documentation:** Keep code well-documented, especially complex algorithms or API interactions. Update relevant parts of the `README.md` and `AGENTS.md` if your changes impact them.

## 4. Pull Request Process

*   **Review:** All Pull Requests will be reviewed by at least one maintainer.
*   **CI Checks:** Ensure all automated checks (CI, linting, testing) pass before submitting a PR.
*   **Responsiveness:** Respond to feedback from reviewers promptly.

## 5. Getting Help

If you have questions or need clarification on any of the contribution guidelines, please open an issue in the repository.

We look forward to your contributions!
