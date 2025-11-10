# Gemini CLI Extension - PostgreSQL

> [!NOTE]
> This extension is currently in beta (pre-v1.0), and may see breaking changes until the first stable release (v1.0).

This Gemini CLI extension provides a set of tools to interact with [PostgreSQL](https://www.postgresql.org/docs/) instances. It allows you to manage your databases, execute queries, and explore schemas directly from the [Gemini CLI](https://google-gemini.github.io/gemini-cli/), using natural language prompts.

Learn more about [Gemini CLI Extensions](https://github.com/google-gemini/gemini-cli/blob/main/docs/extensions/index.md).
> [!IMPORTANT]
> **We Want Your Feedback!**
> Please share your thoughts with us by filling out our feedback [form][form]. 
> Your input is invaluable and helps us improve the project for everyone.

[form]: https://docs.google.com/forms/d/e/1FAIpQLSfEGmLR46iipyNTgwTmIDJqzkAwDPXxbocpXpUbHXydiN1RTw/viewform?usp=pp_url&entry.157487=postgres

## Why Use the Postgres Extension?

* **Natural Language Management:** Stop wrestling with complex commands. Explore schemas and query data by describing what you want in plain English.
* **Seamless Workflow:** Stay in your CLI. No need to constantly switch contexts to the GCP console for common database tasks.
* **Code Generation:** Accelerate development by asking Gemini to generate data classes and other code snippets based on your table schemas.


## Prerequisites

Before you begin, ensure you have the following:

* [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed with version **+v0.6.0**.
* Setup Gemini CLI [Authentication](https://github.com/google-gemini/gemini-cli/tree/main?tab=readme-ov-file#-authentication-options).
* A running PostgreSQL instance.
* User are granted database-level permissions to execute queries.

## Getting Started

### Installation

To install the extension, use the command:

```bash
gemini extensions install https://github.com/gemini-cli-extensions/postgres
```

### Configuration

Set the following environment variables before starting the Gemini CLI. These variables can be loaded from a `.env` file.

```bash
export POSTGRES_HOST="<your-postgres-host>"
export POSTGRES_PORT="<your-postgres-port>"
export POSTGRES_DATABASE="<your-database-name>"
export POSTGRES_USER="<your-database-user>"
export POSTGRES_PASSWORD="<your-database-password>"
```

### Start Gemini CLI

To start the Gemini CLI, use the following command:

```bash
gemini
```

> [!WARNING]
> **Changing Instance & Database Connections**
> Currently, the database connection must be configured before starting the Gemini CLI and can not be changed during a session.
> To save and resume conversation history use command: `/chat save <tag>` and `/chat resume <tag>`.

## Usage Examples

Interact with Postgres using natural language right from your IDE:

* **Explore Schemas and Data:**
    * "Show me all tables in the 'orders' database."
    * "What are the columns in the 'products' table?"
    * "How many orders were placed in the last 30 days, and what were the top 5 most purchased items?"

* **Generate Code:**
    * "Generate a Python dataclass to represent the 'customers' table."

## Supported Tools

 * `list_tables`: Use this tool to lists tables in the database.
 * `execute_sql`: Use this tool to executes a SQL query.
 * `list_active_queries`: Use this tool to list currently running queries.
 * `list_available_extensions`: Use this tool to list available extensions for installation.
 * `list_installed_extensions`: Use this tool to list installed extensions.
 * `get_query_plan`: Use this tool to get query plan.
 * `list_autovacuum_configurations`: Use this tool to list autovacuum configurations and its value.
 * `list_memory_configurations`: Use this tool to list memory configurations and its value.
 * `list_top_bloated_tables`: Use this tool to list top bloated tables.
 * `list_replication_slots`: Use this tool to list replication slots.
 * `list_invalid_indexes`: Use this tool to list invalid indexes.

## Additional Extensions

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions), including:
* [Cloud SQL for PostgreSQL extension](https://github.com/gemini-cli-extensions/cloud-sql-postgresql)
* and more!

## Troubleshooting

Use `gemini --debug` to enable debugging.

Common issues:

* "failed to find default credentials: google: could not find default credentials.": Ensure [Application Default Credentials](https://cloud.google.com/docs/authentication/gcloud) are available in your environment. See [Set up Application Default Credentials](https://cloud.google.com/docs/authentication/external/set-up-adc) for more information.
* "✖ Error during discovery for server: MCP error -32000: Connection closed": The database connection has not been established. Ensure your configuration is set via environment variables.
* "✖ MCP ERROR: Error: spawn /Users/USER/.gemini/extensions/postgres/toolbox ENOENT": The Toolbox binary did not download correctly. Ensure you are using Gemini CLI v0.6.0+.
* "cannot execute binary file": The Toolbox binary did not download correctly. Ensure the correct binary for your OS/Architecture has been downloaded. See [Installing the server](https://googleapis.github.io/genai-toolbox/getting-started/introduction/#installing-the-server) for more information.
