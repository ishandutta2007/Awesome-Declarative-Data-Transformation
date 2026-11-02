# Awesome-Declarative-Data-Transformation

# Awesome-Declarative-Data-Transformation

**Top Declarative Data Transformation (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on SQL-First Modeling, Visual Pipelines, Incremental Materialization & Self-Hosted Transformation Engines*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Declarative Data Transformation**. These tools enable analytics engineers to define *what* the data should look like—not *how* to compute it—with the engine handling dependencies, incremental logic, and materialization—from fully managed cloud platforms with visual canvases to open-source frameworks that give teams version-controlled, testable SQL pipelines.



**Examples** include dbt Cloud, Coalesce.io, Snowflake Dynamic Tables, Materialize, Prophecy.io, Dataform, Matillion, Fivetran Transformations, SQLMesh, and Databricks Delta Live Tables (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted declarative transformation, SQL modeling, and open pipeline frameworks. **Critical note**: The open-source landscape is anchored by **dbt Core**—the de facto standard for SQL-based transformation—and **SQLMesh**—the most significant challenger with virtual environments and column-level lineage. **Dataform** is free but BigQuery-bound. No open-source project matches Coalesce's visual canvas or Prophecy's AI agents, but for declarative SQL modeling, the open-source options are production-proven at scale.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global data integration and declarative transformation sector is estimated at approximately **$16.0B to $19.1B** (2024–2025), expanding at a 12–14% CAGR fueled by cloud analytics and generative AI pipeline demands. The market exhibits a **moderately fragmented**, two-tiered dynamic: hyperscalers and mega-cap platform providers (Google, Databricks, Snowflake) dominate enterprise core infrastructure, while agile, specialized transformation layers (dbt Labs, Fivetran, Coalesce, Materialize) compete aggressively for best-of-breed developer and analytics engineering workloads.

## SaaS/Hosted Platforms

| Platform | Company Valuation / Revenue | Starting Pricing Tier | Free Tier / Trial Limits | Description & Key Trade-offs |
| :--- | :--- | :--- | :--- | :--- |
| **[Dataform](https://cloud.google.com/dataform)** (Google Cloud / Alphabet) | **~$2.0T+ Market Cap** (~$350B+ Revenue) | **$6.25 per TB** (On-demand BigQuery queries; $0.02/GB storage; $0 Dataform service fee) | **Free Forever**: 1 TB queries/month & 10 GB storage free via BigQuery Always Free tier (Plus $300 new GCP account 90-day trial) | SQL-based transformation native to BigQuery with no license fee. **Trade-off**: BigQuery-only; no native multi-cloud or multi-warehouse support. |
| **[Databricks Delta Live Tables](https://www.databricks.com/)** | **$62B–$134B Valuation** (~$3.7B–$4.8B ARR) | **$0.20 to $0.54 per DBU** (Serverless/Classic Core compute rates) | **Free Forever**: Free Edition (1 serverless workspace, 1 small 2X-Small warehouse, daily fair-use quota); **Free Trial**: 14 days with $400 credits | Declarative pipeline framework with streaming and expectations. **Trade-off**: ADVANCED tier pricing wastes DBUs without EXPECT clauses; compute bills scale with cluster sizing. |
| **[Snowflake Dynamic Tables](https://www.snowflake.com/)** | **$45B–$65B Market Cap** (~$3.6B Revenue) | **$2.00 per credit** (Standard Edition virtual warehouse compute rate) | **Free Trial**: 30 days with $400 free credits across virtual warehouse compute and storage | Declarative materialized tables with automated refresh. **Trade-off**: High-frequency target lags incur substantial Cloud Services metadata inspection overheads. |
| **[Fivetran Transformations](https://www.fivetran.com/)** | **$5.6B Valuation** (~$300M+ ARR) | **$0.01 per run** (Tiered from 5,001–30,000 runs; scales down to $0.002/run over 100k runs) | **Free Forever**: Up to 5,000 model runs/month and 500,000 MAR; **Free Trial**: 14 days with unlimited trial syncs & runs | Integrated dbt Core and Quickstart models within managed Fivetran pipelines. **Trade-off**: Optimized primarily for Fivetran connector syncs; large-scale transformations bill per run. |
| **[dbt Cloud](https://www.getdbt.com/)** | **$4.2B Valuation** (~$100M+ ARR) | **$100 per seat/month** (Starter tier, up to 5 seats, includes 15,000 models/month) | **Free Forever**: 1 developer seat with up to 3,000 successful model builds/month; **Free Trial**: 14-day Starter trial | De facto standard managed dbt environment with integrated IDE, scheduler, and semantic layer. **Trade-off**: Seat and model overage costs escalate quickly for scaling teams. |
| **[Matillion](https://www.matillion.com/)** | **$1.5B Valuation** (~$77M–$99M Revenue) | **$2.00 to $2.50 per credit** (Data Productivity Cloud Teams plan starts at ~$20,000/year) | **Free Trial**: 14 days with 500 complimentary Matillion credits | Low-code/visual push-down ETL and in-warehouse transformation platform. **Trade-off**: Cloud data warehouse compute is billed separately on top of Matillion credits. |
| **[Coalesce.io](https://coalesce.io/)** | **$80M–$120M+ Valuation** (~$15M–$25M ARR) | **$150 per user/month** (Starter tier billed annually, up to 4 users, includes 15,000 actions/month) | **Free Forever**: Developer tier with 1 user, 1 project, and 2,000 actions/month; **Free Trial**: 30-day partner/enterprise trial | Column-aware visual transformation canvas built specifically for Snowflake, BigQuery, and Databricks. **Trade-off**: Starter plan caps at 4 transform users; 5+ builders require custom Enterprise. |
| **[Materialize](https://materialize.com/)** | **~$177M Valuation** (~$10M–$15M ARR) | **$1.50 per compute credit** (Cloud On-Demand tier) | **Free Forever**: Self-managed Community License up to 24 GiB RAM and 48 GiB disk; **Free Trial**: 7-day full cloud trial | Real-time streaming SQL database computing incremental materialized views. **Trade-off**: Continuous compute credit charges can accumulate quickly for 24/7 streaming clusters. |
| **[Prophecy.io](https://www.prophecy.ai/)** | **~$70M–$100M Valuation** (~$10M–$30M ARR) | **$150 per user/month** (Professional tier with 50 credits/month; Enterprise Express starts at $4,000/month) | **Free Forever**: Starter edition with 20 credits/month (runs on embedded DuckDB, managed Git) | Visual low-code transformation generating native Spark and SQL code with generative AI agents. **Trade-off**: Credit-based execution limits; multi-engine team deployments require Enterprise tiers. |

## Open-Source GitHub Projects



- **[dbt Core](https://github.com/dbt-labs/dbt-core)**

  **SQL-based transformation framework** (Apache 2.0) — **the de facto standard for declarative SQL modeling**, with the largest ecosystem of packages and community support. **Features**: **SQL SELECT statements** define models; dbt handles materialization (table, view, incremental, ephemeral); **`ref()` and `source()`** for dependency management; **testing framework** (unique, not_null, accepted_values, relationships); **auto-generated documentation and lineage**; **packages** via dbt Hub (dbt-utils, dbt-expectations, etc.); **Jinja templating** for macros and loops . **Tech stack**: Python, SQL. **Deploy**: Self-hosted (dbt Core CLI) or dbt Cloud (managed). **Trade-off**: **Compile time scales superlinearly**—10,000 models take ~35 seconds and 629 MB memory . No built-in virtual environments; requires dbt Cloud for scheduling. **Best for**: analytics engineers wanting the most mature, widely-adopted SQL transformation framework—the default choice for warehouse-native ELT.



- **[SQLMesh](https://github.com/TobikoData/sqlmesh)**

  **Next-generation SQL transformation framework** (Apache 2.0) — **the most significant challenger to dbt**, with virtual environments and column-level lineage. **Features**: **Virtual data environments**—isolated dev/staging without duplicating data or compute; **column-level lineage**; **automatic incremental models**—SQLMesh infers incremental logic; **state-aware orchestration**—only recomputes what changed; **SQLGlot-based transpilation** for multi-dialect support; **Python models** . **Tech stack**: Python, SQL. **Deploy**: Self-hosted (open source) or Tobiko Cloud (managed). **Trade-off**: **Smaller ecosystem than dbt**—fewer packages and community resources; claims 22x faster than dbt-core on Snowflake and 9x on Databricks (vendor benchmarks) . **Best for**: teams frustrated by dbt's compile times and lack of true dev environments—especially those wanting automatic incremental logic and column-level lineage.



- **[Dataform (Open Source)](https://github.com/dataform-co/dataform)**

  **SQL-based transformation for BigQuery** (Apache 2.0) — **the free, BigQuery-native alternative to dbt**. **Features**: **SQLX files** with `ref()` and `config{}` blocks; **assertions** for data quality testing; **declarative tables** and **incremental tables**; **BigQuery-native**—no external scheduler required; **Dataform CLI** for local development . **Tech stack**: JavaScript/TypeScript (CLI), SQLX. **Deploy**: Self-hosted CLI or Google Cloud Dataform (managed). **Trade-off**: **BigQuery-only**—no multi-warehouse support; **smaller ecosystem** than dbt. **Best for**: BigQuery teams wanting free transformation tooling without dbt Cloud costs.



- **[Hydra ETL](https://pypi.org/project/hydra-etl/)**

  **Declarative YAML-based ETL framework** (PyPI package) — **the most accessible open-source ETL/transformation tool** for teams without infrastructure. **Features**: **YAML manifests**—pipelines defined in four files (`sources.yaml`, `transformations.yaml`, `destinations.yaml`, `pipeline.yaml`); **`hdrctl validate`** checks sources, steps, types, and destinations before execution; **DuckDB and pandas engines** per operation; **built-in scheduler** with DAG workflows, retries, and cron triggers; **MCP server** for AI-assisted pipeline authoring; **no Node, no JVM, no container**—single Python process . **Tech stack**: Python. **Deploy**: `pip install hydra-etl[server]`; `hdrctl serve` for Studio UI. **Trade-off**: **File-and-database pipelines only**—not a warehouse-native SQL transformation tool; smaller community than dbt. **Best for**: data engineers wanting declarative ETL without infrastructure—especially those who want YAML pipelines reviewed in pull requests rather than Python scripts .



### Additional Strong Open-Source Options



- **dbt Core (open source)** — The foundation of dbt Cloud, free under Apache 2.0 . **Best for**: teams wanting dbt without the Cloud seat cost.

- **SQLMesh (open source)** — Free Apache 2.0 framework; Tobiko Cloud is the paid managed option . **Best for**: teams wanting dbt alternatives with virtual environments.



**Frameworks for building custom systems**: Combine **dbt Core** for mature SQL modeling with **SQLMesh** for virtual environments and column-level lineage, and **Hydra ETL** for YAML-based ETL pipelines—creating a composable transformation stack. **None of these match Coalesce's visual canvas or Prophecy's AI agents**, but for declarative SQL transformation, the open-source options are production-proven.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Declarative transformation platforms handling production data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.

- **The "SQL-first modeling" vs. "visual canvas" vs. "streaming SQL" vs. "YAML ETL" distinction is critical.** **dbt Core/Cloud and SQLMesh** are **SQL-first modeling**—you write SELECT statements, the framework handles DAG and materialization . **Coalesce and Prophecy** are **visual canvas**—drag-and-drop with generated SQL . **Materialize** is **streaming SQL**—sub-second freshness on event streams . **Hydra ETL** is **YAML ETL**—declarative pipelines for file-and-database workloads . **Snowflake Dynamic Tables** are **declarative materialized views** native to the warehouse . **Choose based on whether you need SQL control, visual building, real-time freshness, or infrastructure-free ETL.**

- **Snowflake Dynamic Tables' Cloud Services costs are the hidden trap.** A pipeline of 200 tables at 1-minute target lag generates **~288,000 change-detection checks daily**—even when no data changes—potentially exceeding the 10% billing threshold . **Increase target lag, use `DOWNSTREAM` for intermediate tables, and suspend non-production tables outside business hours.**

- **dbt Cloud's Enterprise pricing is negotiable but opaque.** Initial quotes are often **20–40% above** final negotiated prices; buyers who credibly evaluate alternatives secure **20–30% discounts** . **Do not accept the first quote.**

- **Coalesce's Starter tier caps at 4 transform users**—teams of 5+ are forced to Enterprise . **Budget accordingly if your team exceeds 4 builders.**

- **Materialize's Community License is genuinely free** up to **24 GiB memory and 48 GiB disk**—the most generous free tier in this category for self-hosted streaming SQL . **The trade-off**: enterprise features require paid license.

- **SQLMesh claims 22x faster than dbt-core on Snowflake** (vendor benchmark), with virtual environments that don't duplicate data . **The trade-off**: smaller ecosystem and fewer packages than dbt.

- **Dataform has no license fee**—you pay only for BigQuery compute and storage . **For BigQuery teams, it is the pragmatic free alternative to dbt Cloud.**

- **Databricks DLT edition mismatch is a silent cost leak.** Paying for ADVANCED without EXPECT clauses, or PRO without CDC, wastes premium DBUs . **Right-size the edition to actual feature usage.**

- **Pricing opacity varies.** dbt Cloud, Coalesce, Materialize, Prophecy, and Fivetran publish tiered or usage pricing. Snowflake Dynamic Tables use Snowflake credits. Matillion and Databricks DLT are consumption-based. **Validate with direct vendor conversations against your model count and freshness requirements.**

- Self-hosted open-source solutions require proper infrastructure (Python for dbt/SQLMesh, warehouses for execution), security hardening, and ongoing maintenance. **Transformation pipelines handle business-critical data**—ensure your deployment meets your organization's reliability and security requirements before migrating production models.



---



**Made for analytics engineers, data teams, and organizations building transparent declarative transformation solutions.**

Let's make Declarative Data Transformation more open, data-driven, and SQL-first.
