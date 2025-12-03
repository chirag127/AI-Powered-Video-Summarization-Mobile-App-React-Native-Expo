# Contributing to VideoSum-AI-Smart-Video-Summarizer-Mobile-App

Thank you for considering contributing to the VideoSum-AI-Smart-Video-Summarizer-Mobile-App project! We welcome your contributions, whether it's bug reports, feature requests, code submissions, or documentation improvements.

## Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code. Please report any violations to `chirag127@example.com`.

## How to Contribute

### 1. Reporting Bugs

*   **Search:** Before reporting a bug, please check if it has already been reported.
*   **Detail:** If not, open a new issue. Provide a clear and concise description of the bug.
*   **Steps to Reproduce:** Include detailed steps to reproduce the behavior.
*   **Environment:** Specify your operating system, device, React Native version, Expo version, and any relevant dependencies.
*   **Screenshots/Videos:** If possible, include screenshots or videos to illustrate the problem.
*   **Use Template:** Use the `bug_report.md` issue template.

### 2. Suggesting Enhancements

*   **Search:** Check if your idea has already been suggested.
*   **Detail:** Open a new issue with a clear description of the feature and why it would be valuable.
*   **Use Template:** Use the `feature_request.md` issue template (if available).

### 3. Pull Requests

We appreciate contributions via pull requests! Follow these steps:

1.  **Fork the Repository:** Create your own fork of the `chirag127/VideoSum-AI-Smart-Video-Summarizer-Mobile-App` repository.
2.  **Clone Your Fork:** `git clone https://github.com/YOUR_USERNAME/VideoSum-AI-Smart-Video-Summarizer-Mobile-App.git`
3.  **Create a Branch:** Create a descriptive branch for your changes: `git checkout -b feature/your-feature-name` or `bugfix/your-bug-fix`.
4.  **Install Dependencies:** Ensure you have the necessary dependencies installed:
    bash
    npx expo install
    # or
    yarn install
    
5.  **Make Changes:** Implement your feature or fix your bug.
6.  **Test Your Changes:** Run tests to ensure your changes don't break existing functionality:
    bash
    npx jest --ci
    # or
    yarn test --ci
    
    Ensure all tests pass. If adding new functionality, consider adding new tests.
7.  **Lint and Format:** Ensure your code adheres to the project's coding standards:
    bash
    npx biome lint --apply
    npx biome format --write
    # or if using ESLint/Prettier
    yarn lint --fix
    yarn format
    
8.  **Commit Your Changes:** Write clear, concise commit messages. Follow conventional commits if applicable.
    bash
    git add .
    git commit -m "feat: Add awesome new feature"
    
9.  **Push to Your Fork:** `git push origin feature/your-feature-name`
10. **Open a Pull Request:** Navigate to the original repository (`https://github.com/chirag127/VideoSum-AI-Smart-Video-Summarizer-Mobile-App`) and open a new pull request from your feature branch.
    *   **Title:** Provide a clear title for your PR.
    *   **Description:** Explain what your changes do, why they are necessary, and how you tested them.
    *   **Link Issues:** Reference any related issues (e.g., `Closes #123`).

### 4. Development Environment Setup

To set up the project locally for development, follow these steps:

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/VideoSum-AI-Smart-Video-Summarizer-Mobile-App.git
    cd VideoSum-AI-Smart-Video-Summarizer-Mobile-App
    
2.  **Install Node.js and npm/yarn:** Ensure you have Node.js (v18+) and a package manager (npm or Yarn) installed.
3.  **Install Project Dependencies:**
    bash
    npm install
    # or
    yarn install
    
4.  **Install Expo Go (Mobile App):** Download the Expo Go app on your physical iOS or Android device from the respective app store.
5.  **Run the Development Server:**
    bash
    npx expo start
    # or
    yarn start
    
    This will start the Metro bundler and display a QR code. Scan this QR code using the Expo Go app on your device to run the application.

### 5. Project Structure and Architecture

This project follows a modular architecture, leveraging React Native and Expo for cross-platform development.

*   **`src/`**: Contains the core application logic.
    *   **`components/`**: Reusable UI components.
    *   **`screens/`**: Application screens.
    *   **`services/`**: API interactions and business logic.
    *   **`utils/`**: Helper functions.
    *   **`navigation/`**: Navigation setup.
*   **`assets/`**: Static assets like images and fonts.
*   **`constants/`**: Application-wide constants.

**AI Integration:** Key AI functionalities, such as video summarization, are handled by dedicated modules within the `services/` directory, interacting with external AI APIs.

## Guidelines & Principles

*   **SOLID Principles:** Strive to apply SOLID principles in your code.
*   **DRY (Don't Repeat Yourself):** Avoid redundant code. Abstract common logic into reusable functions or components.
*   **YAGNI (You Ain't Gonna Need It):** Implement only what is necessary now. Avoid over-engineering.
*   **TypeScript First:** Utilize TypeScript for strong typing and improved code maintainability.
*   **Testing:** Write comprehensive unit and integration tests for new features and bug fixes.
*   **Code Reviews:** All pull requests will undergo a code review process. Be open to feedback and suggestions.

## Submitting an Issue

When submitting an issue, please use the provided issue templates (`bug_report.md`, `feature_request.md`). Ensure your issue is well-documented and provides sufficient information for us to understand and resolve it.

## Thank You!

Your contributions help make `VideoSum-AI-Smart-Video-Summarizer-Mobile-App` better for everyone. We look forward to your contributions!
