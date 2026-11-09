# Dactopus

An open data foundation for e-commerce on ClickHouse: canonical tables of a store and its web analytics, the semantic models that describe them to AI agents, and the process that keeps them up to date. Three repositories, all under the Apache License 2.0.

| Repository | What it is | Start here if |
| --- | --- | --- |
| [dactopus-data-models](https://github.com/Dactopus/dactopus-data-models) | Canonical entities (orders, order lines, refunds, customers, products; sessions, events, purchases) as Apache Ossie semantic models, and the dbt packages that build their tables from Shopify, WooCommerce and GA4 | you want to see what the data looks like |
| [dactopus-ossie-clickhouse](https://github.com/Dactopus/dactopus-ossie-clickhouse) | Executes Apache Ossie models on ClickHouse: answers a question asked in metrics, dimensions and filters with one query, and serves the model to AI agents over MCP | you have a model and want to ask it questions |
| [dactopus](https://github.com/Dactopus/dactopus) | The runner a client installs next to their ClickHouse: loads the sources, builds and checks the tables, serves the models | you want this to run on a schedule |

The entities have the same shape whatever the data came from: a store on Shopify and a store on WooCommerce answer the same question with the same query.

## Try it in an hour

The [Quick start](https://github.com/Dactopus/dactopus-data-models#quick-start) of dactopus-data-models builds the Shopify package over the rows the repository tests it with, checks the commerce model's numbers against them, and serves the model to an AI agent. It needs a ClickHouse, dbt and the executor.

## Questions

Questions and ideas go to [Discussions](https://github.com/orgs/Dactopus/discussions). A number you believe is wrong is an issue in the repository that produced it. Say the source and entity, the question, the number you got, the one you expected, and where the expected one comes from.

## Status

Every repository is below 1.0 and follows SemVer: a minor release may change interfaces, and each changelog says what.
