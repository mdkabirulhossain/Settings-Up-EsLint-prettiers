"# Setting Up ESLint & Prettier in a Node.js Project (VS Code)"

This guide will help you set up ESLint and Prettier for code linting and formatting in your project.</br>

Step 1: Install ESLint and Prettier
Run the following command in your project directory to install both ESLint and Prettier:
<strong>npm install eslint prettier eslint-config-prettier eslint-plugin-prettier --save-dev</strong>
What These Packages Do:
eslint – Lints your code for errors and best practices.
prettier – Automatically formats your code.
eslint-config-prettier – Disables ESLint rules that conflict with Prettier.
eslint-plugin-prettier – Runs Prettier as an ESLint rule. </br></br>
Step 2: Configure ESLint
Since you've already created .eslintrc.json, update it with this configuration:

📄 .eslintrc.json

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
→ Ensures files follow Prettier formatting. </br>

Step 3: Install VS Code Extensions
To get real-time feedback, install these VS Code extensions:

ESLint – Helps with linting.
Prettier - Code formatter – Formats code automatically.
✅ Install them from the VS Code Extensions Marketplace. </br> </br>

Step 4: Enable Auto-Fixing & Formatting in VS Code
Open VS Code Settings (Ctrl + , or Cmd + , on macOS).
Search for "Format On Save" and enable it.
Go to Settings JSON and add:

{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
Restart VS Code.
