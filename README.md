# TodoList

This repository contains the standalone Angular frontend for the Todo service. The project was originally part of the `todo-service` backend but has been extracted so it can be developed and deployed independently.

The UI is built with Angular 19.2 and includes the following features:

- Todo list management
- Finance module with account and transaction views
- Navigation bar and routing configuration
- Hot module replacement (HMR) during development

## Getting started

```bash
# install dependencies (run once)
npm install

# start development server
npm start
```

The app will be served at `http://localhost:4200/`. Changes to source files automatically reload the page.

## Project structure

```
src/
  app/
    todo-list/            # todo list component
    finance/              # finance feature module
    nav/                  # navigation bar
  index.html
  main.ts
  styles.css
```

## Repository history

This project was moved out of the monolithic backend repository (`todo-service`) on 2026-02-28. All frontend code lives here, and the GitHub repository is available at:

https://github.com/vreddy-pv/todo-list.git

## Further development

Use the Angular CLI to generate new components or services:

```bash
ng generate component my-component
```

When ready, build for production with:

```bash
ng build --configuration production
```

```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Karma](https://karma-runner.github.io) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.


# API Documentation

  ## Transactions

  ### Process a Transaction
  **Endpoint**: `POST /transactions`

  **Request Body**:
  ```json
  {
    "accountId": "string",
    "amount": number,
    "type": "deposit" | "withdrawal"
  }

  Response:
  {
    "message": "string",
    "account": {
      "id": "string",
      "balance": number
    }
  }

  Example:
  curl -X POST http://localhost:3000/transactions \
  -H "Content-Type: application/json" \
  -d '{"accountId": "123", "amount": 200, "type": "deposit"}'

  **Action:**

  Use the `Write` tool to save the above content to `API.md`.

  ```json
  {
    "file_path": "C:\\Veera\\AI\\claude-code\\todo-service\\todo-list\\API.md",
    "content": "# API Documentation\n\n## Transactions\n\n### Process a Transaction\n**Endpoint**: `POST /transactions`\n\n**Request
  Body**:\n```json\n{\n  \"accountId\": \"string\",\n  \"amount\": number,\n  \"type\": \"deposit\" |
  \"withdrawal\"\n}\n```\n\n**Response**:\n```json\n{\n  \"message\": \"string\",\n  \"account\": {\n    \"id\": \"string\",\n    \"balance\": 
  number\n  }\n}\n```\n\n**Example**:\n```bash\ncurl -X POST http://localhost:3000/transactions \\\n-H \"Content-Type: application/json\"      
  \\\n-d '{\"accountId\": \"123\", \"amount\": 200, \"type\": \"deposit\"}'\n```"
  }

  ---