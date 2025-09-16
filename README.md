# Gemini CLI Extension - PostgreSQL

This Gemini CLI extension provides a set of tools to interact with [PostgreSQL](https://www.postgresql.org/docs/) instances. It allows you to manage your databases, execute queries, and explore schemas directly from the [Gemini CLI](https://google-gemini.github.io/gemini-cli/), using natural language prompts.

## Features

*   **Integrated with Gemini CLI:** As a Google-developed extension, it integrates seamlessly into the Gemini CLI environment, making security an accessible part of your workflow.
*   **Connect to PostgreSQL:** Securely connect to your PostgreSQL instances.
*   **Explore Database Schema:** List databases, tables, views, and schemas.
*   **Query your Database:** Execute SQL queries against your database.

## Prerequisites

Before you begin, ensure you have the following:

*   [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed.
*   A running PostgreSQL instance.
*   User are granted database-level permissions to execute queries.

## Installation

To install the extension, use the command:

```bash
gemini extensions install github.com/gemini-cli-extensions/postgresql.git
```

## Configuration

*   `POSTGRES_HOST`: The hostname or IP address of the PostgreSQL server.
*   `POSTGRES_PORT`: The port number of the PostgreSQL server.
*   `POSTGRES_DATABASE`: The name of the database to connect to.
*   `POSTGRES_USER`: The username for authentication.
*   `POSTGRES_PASSWORD`: The password for authentication.


## Usage

* Explore Schemas and Data
* Generate code

## Supported Tools

* `list_tables`: Use this tool to list tables and descriptions.
* `execute_sql`: Use this tool to execute any SQL statement.

## Security

This extension executes commands against your PostgreSQL database. Always review the generated SQL queries before execution, especially for write operations.