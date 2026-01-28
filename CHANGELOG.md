# Changelog

## [0.2.0](https://github.com/gemini-cli-extensions/postgres/compare/0.1.5...0.2.0) (2026-01-26)


### ⚠ BREAKING CHANGES

* Validate tool naming ([genai-toolbox#​2305](https://redirect.github.com/googleapis/genai-toolbox/issues/2305)) ([5054212](https://redirect.github.com/googleapis/genai-toolbox/commit/5054212fa43017207fe83275d27b9fbab96e8ab5))

### Features

* **prebuilt/cloud-sql:** Add create backup tool for Cloud SQL ([genai-toolbox#​2141](https://redirect.github.com/googleapis/genai-toolbox/issues/2141)) ([8e0fb03](https://redirect.github.com/googleapis/genai-toolbox/commit/8e0fb0348315a80f63cb47b3c7204869482448f4)) ([515afdc](https://github.com/gemini-cli-extensions/postgres/commit/515afdcdbaad85fe7fd89162d3c0c080d38e8a18))
* **prebuilt/cloud-sql:** Add restore backup tool for Cloud SQL ([genai-toolbox#​2171](https://redirect.github.com/googleapis/genai-toolbox/issues/2171)) ([00c3e6d](https://redirect.github.com/googleapis/genai-toolbox/commit/00c3e6d8cba54e2ab6cb271c7e6b378895df53e1)) ([515afdc](https://github.com/gemini-cli-extensions/postgres/commit/515afdcdbaad85fe7fd89162d3c0c080d38e8a18))
* **tools/postgres:** Add additional filter params for existing postgres tools ([genai-toolbox#​2033](https://redirect.github.com/googleapis/genai-toolbox/issues/2033)) ([489117d](https://redirect.github.com/googleapis/genai-toolbox/commit/489117d74711ac9260e7547163ca463eb45eeaa2)) ([328dca4](https://github.com/gemini-cli-extensions/postgres/commit/328dca4b1a632c5bc5f6d3bd67862574b8f8c426))
* **tools/postgres:** Add list\_pg\_settings, list\_database\_stats tools for postgres ([genai-toolbox#​2030](https://redirect.github.com/googleapis/genai-toolbox/issues/2030)) ([32367a4](https://redirect.github.com/googleapis/genai-toolbox/commit/32367a472fae9653fed7f126428eba0252978bd5)) ([328dca4](https://github.com/gemini-cli-extensions/postgres/commit/328dca4b1a632c5bc5f6d3bd67862574b8f8c426))
* **tools/postgres:** Add new postgres-list-roles tool ([genai-toolbox#​2038](https://redirect.github.com/googleapis/genai-toolbox/issues/2038)) ([bea9705](https://redirect.github.com/googleapis/genai-toolbox/commit/bea97054502cfa236aa10e2ebc8ff58eb00ad035)) ([328dca4](https://github.com/gemini-cli-extensions/postgres/commit/328dca4b1a632c5bc5f6d3bd67862574b8f8c426))
* **tools/postgressql:** Add Parameter `embeddedBy` config support ([genai-toolbox#​2151](https://redirect.github.com/googleapis/genai-toolbox/issues/2151)) ([17b70cc](https://redirect.github.com/googleapis/genai-toolbox/commit/17b70ccaa754d15bcc33a1a3ecb7e652520fa600)) ([328dca4](https://github.com/gemini-cli-extensions/postgres/commit/328dca4b1a632c5bc5f6d3bd67862574b8f8c426))
* **tools/postgressql:** Add tool to list store procedure ([genai-toolbox#​2156](https://redirect.github.com/googleapis/genai-toolbox/issues/2156)) ([cf0fc51](https://redirect.github.com/googleapis/genai-toolbox/commit/cf0fc515b57d9b84770076f3c0c5597c4597ef62)) ([328dca4](https://github.com/gemini-cli-extensions/postgres/commit/328dca4b1a632c5bc5f6d3bd67862574b8f8c426))
* Support MCP specs version 2025-11-25 ([genai-toolbox#​2303](https://redirect.github.com/googleapis/genai-toolbox/issues/2303)) ([4d23a3b](https://redirect.github.com/googleapis/genai-toolbox/commit/4d23a3bbf2797b1f7fe328aeb5789e778121da23)) ([515afdc](https://github.com/gemini-cli-extensions/postgres/commit/515afdcdbaad85fe7fd89162d3c0c080d38e8a18))
* Validate tool naming ([genai-toolbox#​2305](https://redirect.github.com/googleapis/genai-toolbox/issues/2305)) ([5054212](https://redirect.github.com/googleapis/genai-toolbox/commit/5054212fa43017207fe83275d27b9fbab96e8ab5)) ([515afdc](https://github.com/gemini-cli-extensions/postgres/commit/515afdcdbaad85fe7fd89162d3c0c080d38e8a18))


### Bug Fixes

* List tables tools null fix ([genai-toolbox#​2107](https://redirect.github.com/googleapis/genai-toolbox/issues/2107)) ([2b45266](https://redirect.github.com/googleapis/genai-toolbox/commit/2b452665983154041d4cd0ed7d82532e4af682eb)) ([328dca4](https://github.com/gemini-cli-extensions/postgres/commit/328dca4b1a632c5bc5f6d3bd67862574b8f8c426))

## [0.1.5](https://github.com/gemini-cli-extensions/postgres/compare/0.1.4...0.1.5) (2025-12-08)


### Features

* **tools/postgres-list-publication-tables:** Add new postgres-list-publication-tables tool ([genai-toolbox#​1919](https://redirect.github.com/googleapis/genai-toolbox/issues/1919)) ([f4b1f0a](https://redirect.github.com/googleapis/genai-toolbox/commit/f4b1f0a68000ca2fc0325f55a1905705417c38a2)) ([2c3714e](https://github.com/gemini-cli-extensions/postgres/commit/2c3714ed3868e8264b8d1a41bd23261d781fa260))
* **tools/postgres-list-tablespaces:** Add new postgres-list-tablespaces tool ([genai-toolbox#​1934](https://redirect.github.com/googleapis/genai-toolbox/issues/1934)) ([5ad7c61](https://redirect.github.com/googleapis/genai-toolbox/commit/5ad7c6127b3e47504fc4afda0b7f3de1dff78b8b)) ([2c3714e](https://github.com/gemini-cli-extensions/postgres/commit/2c3714ed3868e8264b8d1a41bd23261d781fa260))
* **tools/postgres:** Add list-query-stats and get-column-cardinality functions ([genai-toolbox#​1976](https://redirect.github.com/googleapis/genai-toolbox/issues/1976)) ([9f76026](https://redirect.github.com/googleapis/genai-toolbox/commit/9f760269253a8cc92a357e995c6993ccc4a0fb7b)) ([2c3714e](https://github.com/gemini-cli-extensions/postgres/commit/2c3714ed3868e8264b8d1a41bd23261d781fa260))

## [0.1.4](https://github.com/gemini-cli-extensions/postgres/compare/0.1.3...0.1.4) (2025-12-01)


### Features

* **tools/postgres:** Add `long_running_transactions`, `list_locks` and `replication_stats` tools ([genai-toolbox#​1751](https://redirect.github.com/googleapis/genai-toolbox/issues/1751)) ([5abad5d](https://redirect.github.com/googleapis/genai-toolbox/commit/5abad5d56c6cc5ba86adc5253b948bf8230fa830)) ([159f7d5](https://github.com/gemini-cli-extensions/postgres/commit/159f7d50673345dcec96903e90a8fd9d6383582f))


### Bug Fixes

* **tools:** Check for query execution error for pgxpool.Pool ([genai-toolbox#​1969](https://redirect.github.com/googleapis/genai-toolbox/issues/1969)) ([2bff138](https://redirect.github.com/googleapis/genai-toolbox/commit/2bff1384a3570ef46bc03ebebc507923af261987)) ([159f7d5](https://github.com/gemini-cli-extensions/postgres/commit/159f7d50673345dcec96903e90a8fd9d6383582f))

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
