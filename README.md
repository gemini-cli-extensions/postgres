# Gemini CLI Extension - PostgreSQL

> [!NOTE]
> This extension is currently in beta (pre-v1.0), and may see breaking changes until the first stable release (v1.0).

This Gemini CLI extension provides a set of tools to interact with [PostgreSQL](https://www.postgresql.org/docs/) instances. It allows you to manage your databases, execute queries, and explore schemas directly from the [Gemini CLI](https://google-gemini.github.io/gemini-cli/), using natural language prompts.

Learn more about [Gemini CLI Extensions](https://github.com/google-gemini/gemini-cli/blob/main/docs/extension.md).

## Why Use the Postgres Extension?

*   **Natural Language Management:** Stop wrestling with complex commands. Explore schemas and query data by describing what you want in plain English.
*   **Seamless Workflow:** Stay in your CLI. No need to constantly switch contexts to the GCP console for common database tasks.
*   **Code Generation:** Accelerate development by asking Gemini to generate data classes and other code snippets based on your table schemas.

## Prerequisites

Before you begin, ensure you have the following:

*   [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed with version **+v0.6.0**.
*   A running PostgreSQL instance.
*   User are granted database-level permissions to execute queries.

## Installation

To install the extension, use the command:

```bash
gemini extensions install https://github.com/gemini-cli-extensions/postgres
```

## Configuration

Set the following environment variables before starting the Gemini CLI:

*   `POSTGRES_HOST`: The hostname or IP address of the PostgreSQL server.
*   `POSTGRES_PORT`: The port number of the PostgreSQL server.
*   `POSTGRES_DATABASE`: The name of the database to connect to.
*   `POSTGRES_USER`: The username for authentication.
*   `POSTGRES_PASSWORD`: The password for authentication.

## Usage Examples

Interact with Postgres using natural language right from your IDE:

*   **Explore Schemas and Data:**
    * "Show me all tables in the 'orders' database."
    * "What are the columns in the 'products' table?"
    * "How many orders were placed in the last 30 days, and what were the top 5 most purchased items?"

*   **Generate Code:**
    * "Generate a Python dataclass to represent the 'customers' table."

## Supported Tools

 * `list_tables`: Use this tool to lists tables in the database.
 * `execute_sql`: Use this tool to executes a SQL query.
 * `list_active_queries`: Use this tool to list currently running queries.
 * `list_available_extensions`: Use this tool to list available extensions for installation.
 * `list_installed_extensions`: Use this tool to list installed extensions.
 * `get_query_plan`: Use this tool to get query plan.
 * `list_autovacuum_configurations`: Use this tool to list autovacuum configurations and its value.
 * `list_memory_configuration`s: Use this tool to list memory configurations and its value.
 * `list_top_bloated_tables`: Use this tool to list top bloated tables.
 * `list_replication_slots`: Use this tool to list replication slots.
 * `list_invalid_indexes`: Use this tool to list invalid indexes.

## Additional Extensions

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions).

## Troubleshooting

* "cannot execute binary file": Ensure the correct binary for your OS/Architecture has been downloaded. See [Installing the server](https://googleapis.github.io/genai-toolbox/getting-started/introduction/#installing-the-server) for more information.
