"# Setting Up ESLint & Prettier in a Node.js Project (VS Code)"

This guide will help you set up ESLint and Prettier for code linting and formatting in your project.</br>

Step 1: Install ESLint and Prettier
Run the following command in your project directory to install both ESLint and Prettier:
<strong>npm install eslint prettier eslint-config-prettier eslint-plugin-prettier --save-dev</strong>
What These Packages Do:
eslint – Lints your code for errors and best practices.
prettier – Automatically formats your code.
eslint-config-prettier – Disables ESLint rules that conflict with Prettier.
eslint-plugin-prettier – Runs Prettier as an ESLint rule. </br>
Step 2: Configure ESLint
Since you've already created .eslintrc.json, update it with this configuration:

📄 .eslintrc.json

json
Copy
Edit
{
  "env": {
    "browser": true,
    "es2021": true,
    "node": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:prettier/recommended"
  ],
  "rules": {
    "prettier/prettier": ["error", { "endOfLine": "auto" }]
  }
}
Explanation:
"extends": ["eslint:recommended", "plugin:prettier/recommended"]
→ Uses recommended ESLint rules and integrates Prettier.
"prettier/prettier": ["error", { "endOfLine": "auto" }]
→ Ensures files follow Prettier formatting.

