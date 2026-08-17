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

* One of the supported agent harnesses, installed and authenticated:
  * [Gemini CLI](https://github.com/google-gemini/gemini-cli) (v0.6.0+)
  * [Claude Code](https://code.claude.com)
  * [Codex](https://developers.openai.com/codex)
  * [Antigravity CLI](https://antigravity.google)
* [Node.js](https://nodejs.org/) (the MCP server runs via `npx`).
* A running PostgreSQL instance.
* Users are granted database-level permissions to execute queries.

## Getting Started

### Installation

All harnesses use the same plugin; the MCP server runs via `npx` (no binary to download). Install with your harness of choice:

**Gemini CLI**

```bash
gemini extensions install https://github.com/gemini-cli-extensions/postgres
```

**Claude Code**

```bash
claude plugin marketplace add gemini-cli-extensions/postgres
claude plugin install postgres@postgres
```

**Codex**

```bash
codex plugin marketplace add gemini-cli-extensions/postgres
codex plugin add postgres@postgres
```

**Antigravity**

```bash
agy plugin install https://github.com/gemini-cli-extensions/postgres
```

See [Configuration](#configuration) for how each harness supplies the connection settings.

### Configuration

The plugin connects to PostgreSQL using these settings:

*   `POSTGRES_DATABASE`: The name of the database to connect to.
*   `POSTGRES_USER`: The database username.
*   `POSTGRES_PASSWORD`: The password for the database user.
*   `POSTGRES_HOST`: (Optional) The Postgres host. Defaults to `localhost`.
*   `POSTGRES_PORT`: (Optional) The Postgres port. Defaults to `5432`.
*   `POSTGRES_QUERY_PARAMS`: (Optional) Connection string parameters.

How you supply them depends on the harness:

*   **Gemini CLI**: prompted on install and saved to the extension's `.env`. View or update later with `gemini extensions list` / `gemini extensions config postgres [setting] [--scope user|workspace]` (restart the CLI to apply).
*   **Claude Code**: pass `--config KEY=VALUE` on install (repeatable), or run `/plugin` inside Claude Code.
*   **Codex** and **Antigravity**: export the variables in your shell before starting:

```bash
export POSTGRES_DATABASE="<your-database-name>"
export POSTGRES_USER="<your-database-user>"
export POSTGRES_PASSWORD="<your-database-password>"
export POSTGRES_HOST="<your-postgres-host>"                    # Optional, defaults to localhost
export POSTGRES_PORT="<your-postgres-port>"                    # Optional, defaults to 5432
export POSTGRES_QUERY_PARAMS="<your-connection-string-params>" # Optional
```

> [!NOTE]
> See [Troubleshooting](#troubleshooting) for debugging your configuration.

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

 * `list_tables`: Use this tool to list tables in the database.
 * `database_overview`: Use this tool to fetches the current state of the PostgreSQL server.
 * `execute_sql`: Use this tool to execute a SQL query.
 * `list_active_queries`: Use this tool to list currently running queries.
 * `list_available_extensions`: Use this tool to list available extensions for installation.
 * `list_installed_extensions`: Use this tool to list installed extensions.
 * `get_query_plan`: Use this tool to get query plan.
 * `list_autovacuum_configurations`: Use this tool to list autovacuum configurations and its value.
 * `list_database_stats`: Use this tool to lists the key performance and activity statistics for each database in the PostgreSQL server.
 * `list_indexes`: Use this tool to list available user indexes in a PostgreSQL database.
 * `list_memory_configurations`: Use this tool to list memory configurations and its value.
 * `list_pg_settings`: Use this tool to list configuration parameters for the PostgreSQL server.
 * `list_publication_tables`: Use this tool to list publication tables in a PostgreSQL database.
 * `list_replication_slots`: Use this tool to list replication slots.
 * `list_roles`: Use this tool to lists all the user-created roles in PostgreSQL database.
 * `list_schemas`: Use this tool to lists schemas in the database.
 * `list_sequences`: Use this tool to list sequences in a PostgreSQL database.
 * `list_tablespaces`: Use this tool to lists tablespaces in the database.
 * `list_top_bloated_tables`: Use this tool to list top bloated tables.
 * `list_triggers`: Use this tool to lists triggers in the database.
 * `list_views`: Use this tool to lists views in the database from pg_views with a default limit of 50 rows.
 * `list_invalid_indexes`: Use this tool to list invalid indexes.

## Additional Extensions

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions), including:
* [Cloud SQL for PostgreSQL extension](https://github.com/gemini-cli-extensions/cloud-sql-postgresql)
* and more!

## Troubleshooting

Use `gemini --debug` to enable debugging.

Common issues:

* "✖ Error during discovery for server: MCP error -32000: Connection closed": The database connection has not been established. Ensure your configuration is set via environment variables.
* "✖ MCP ERROR: Error: spawn npx ENOENT": Node.js/`npx` is not installed or not on your `PATH`. Install Node.js (which provides `npx`).
* "npm error"/network failures on first run: `npx` fetches `@toolbox-sdk/server` on first launch, so it needs network access. Retry once connectivity is available.
