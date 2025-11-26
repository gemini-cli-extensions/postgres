# Changelog

## [0.1.3](https://github.com/gemini-cli-extensions/postgres/compare/0.1.2...0.1.3) (2025-11-18)


### Features

* **source/alloydb, source/cloud-sql-postgres,source/cloud-sql-mysql,source/cloud-sql-mssql:** Use project from env for alloydb and cloud sql control plane tools ([genai-toolbox#​1588](https://redirect.github.com/googleapis/genai-toolbox/issues/1588)) ([12bdd95](https://redirect.github.com/googleapis/genai-toolbox/commit/12bdd954597e49d3ec6b247cc104584c5a4d1943)) ([89a0789](https://github.com/gemini-cli-extensions/postgres/commit/89a0789c18d0b66b4ae14febf19ae3a1ffb4c06e))
* **source/Postgresql:** Set default host and port for Postgresql  source ([genai-toolbox#​1927](https://redirect.github.com/googleapis/genai-toolbox/issues/1927)) ([7e6e88a](https://redirect.github.com/googleapis/genai-toolbox/commit/7e6e88a21f2b9b60e0d645cdde33a95892d31a04)) ([89a0789](https://github.com/gemini-cli-extensions/postgres/commit/89a0789c18d0b66b4ae14febf19ae3a1ffb4c06e))
* **tools/postgres:** Add `list_triggers`, `database_overview` tools for postgres ([genai-toolbox#​1912](https://redirect.github.com/googleapis/genai-toolbox/issues/1912)) ([a4c9287](https://redirect.github.com/googleapis/genai-toolbox/commit/a4c9287aecf848faa98d973a9ce5b13fa309a58e)) ([89a0789](https://github.com/gemini-cli-extensions/postgres/commit/89a0789c18d0b66b4ae14febf19ae3a1ffb4c06e))
* **tools/postgres:** Add list\_indexes, list\_sequences tools for postgres ([genai-toolbox#​1765](https://redirect.github.com/googleapis/genai-toolbox/issues/1765)) ([897c63d](https://redirect.github.com/googleapis/genai-toolbox/commit/897c63dcea43226262d2062088c59f2d1068fca7)) ([89a0789](https://github.com/gemini-cli-extensions/postgres/commit/89a0789c18d0b66b4ae14febf19ae3a1ffb4c06e))
* Added prompt support for toolbox ([genai-toolbox#​1798](https://redirect.github.com/googleapis/genai-toolbox/issues/1798)) ([cd56ea4](https://redirect.github.com/googleapis/genai-toolbox/commit/cd56ea44fbdd149fcb92324e70ee36ac747635db)) ([89a0789](https://github.com/gemini-cli-extensions/postgres/commit/89a0789c18d0b66b4ae14febf19ae3a1ffb4c06e))

## [0.1.2](https://github.com/gemini-cli-extensions/postgres/compare/0.1.1...0.1.2) (2025-11-07)


### Features

* **tools/postgres-list-schemas:** Add new postgres-list-schemas tool ([genai-toolbox#​1741](https://redirect.github.com/googleapis/genai-toolbox/issues/1741)) ([1a19cac](https://redirect.github.com/googleapis/genai-toolbox/commit/1a19cac7cd89ed70291eb55e190370fe7b2c1aba)) ([6876ee4](https://github.com/gemini-cli-extensions/postgres/commit/6876ee4b2a1b9e932bd42c9bee148b8d66873749))
* **tools/postgres-list-views:** Add new postgres-list-views tool ([genai-toolbox#​1709](https://redirect.github.com/googleapis/genai-toolbox/issues/1709)) ([e8c7fe0](https://redirect.github.com/googleapis/genai-toolbox/commit/e8c7fe0994fedcb9be78d461fab3c98cc6bd86b2)) ([6876ee4](https://github.com/gemini-cli-extensions/postgres/commit/6876ee4b2a1b9e932bd42c9bee148b8d66873749))


### Bug Fixes

* **tools/postgres-execute-sql:** Do not ignore SQL failure ([genai-toolbox#​1829](https://redirect.github.com/googleapis/genai-toolbox/issues/1829)) ([8984287](https://redirect.github.com/googleapis/genai-toolbox/commit/898428759c2a1a384bea8939605cf0914d129bec)) ([6876ee4](https://github.com/gemini-cli-extensions/postgres/commit/6876ee4b2a1b9e932bd42c9bee148b8d66873749))

## [0.1.1](https://github.com/gemini-cli-extensions/postgres/compare/0.1.0...0.1.1) (2025-09-30)


### Features

* additional instructions for the context file ([#26](https://github.com/gemini-cli-extensions/postgres/issues/26)) ([96f8337](https://github.com/gemini-cli-extensions/postgres/commit/96f83373f5694367b8a9ac605617dcfc85ed1926))
* standardize mcp server names ([#24](https://github.com/gemini-cli-extensions/postgres/issues/24)) ([2810ce4](https://github.com/gemini-cli-extensions/postgres/commit/2810ce4a3fb29394d5bc65eefef8d2ed46f3e8e9))
* update context file to guide on changing resources ([db50b17](https://github.com/gemini-cli-extensions/postgres/commit/db50b17570815827784bf78de43136298b4931b9))
* update context file to recommend full table name ([#27](https://github.com/gemini-cli-extensions/postgres/issues/27)) ([3f109bc](https://github.com/gemini-cli-extensions/postgres/commit/3f109bc278862390083269a6a96fd016548a636f))

## 0.1.0 (2025-09-21)


### Features

* Add Postgres Extension
