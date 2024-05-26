# Doctors Galaxy

## Description

Doctors Galaxy is an automated testing project designed to ensure the functionality and reliability of the Doctors Galaxy website. The project uses Playwright with JavaScript to simulate user interactions and verify that the website performs as expected across different scenarios.

## Technologies and Techniques

-   **Playwright**: A Node.js library to automate browsers (Chromium, Firefox, and WebKit) with a single API.
-   **JavaScript**: The primary programming language used for writing the automation scripts.
-   **Node.js**: The runtime environment for executing JavaScript code on the server-side.
-   **npm**: The package manager for Node.js, used to install and manage dependencies.

## Prerequisites

-   Node.js (version 12 or higher)
-   npm (comes with Node.js)

## Setup Instructions

1. **Clone the Repository**

    ```sh
    git clone https://github.com/your-username/doctors-galaxy.git
    cd doctors-galaxy
    ```

2. **Install Dependencies**

    ```sh
    npm install
    ```

3. **Run the Tests**
   To execute the tests, use the following command:
    ```sh
    npx playwright test
    ```

## Project Structure

-   `tests/`: Contains all test scripts.
-   `playwright.config.js`: Configuration file for Playwright.
-   `package.json`: Lists project dependencies and scripts.
-   `README.md`: Project documentation.

## Writing and Running Tests

1. **Creating a Test File**
   Inside the `tests/` directory, create a new test file, for example, `example.spec.js`:

    ```js
    const { test, expect } = require("@playwright/test");

    test("basic test", async ({ page }) => {
        await page.goto("https://www.your-website.com");
        await expect(page).toHaveTitle("Your Website Title");
    });
    ```

2. **Running a Specific Test**
   To run a specific test file, use:

    ```sh
    npx playwright test tests/example.spec.js
    ```

3. **Generating Test Reports**
   Playwright provides options to generate reports. You can configure this in `playwright.config.js`:
    ```js
    module.exports = {
        reporter: [["list"], ["json", { outputFile: "test-results.json" }]],
    };
    ```

## Additional Resources

-   [Playwright Documentation](https://playwright.dev/docs/intro)
-   [Node.js Documentation](https://nodejs.org/en/docs/)
-   [npm Documentation](https://docs.npmjs.com/)

Feel free to contribute to the project by submitting issues or pull requests. Happy testing!
