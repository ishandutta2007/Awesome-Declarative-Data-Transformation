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

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[dbt Cloud](https://www.getdbt.com/)**

  **Managed dbt platform** with IDE, scheduler, and CI. **Pricing**: **Developer (free)** for 1 seat with **3,000 successful models/month**; **Starter $100/seat/month** with 5 seats and **15,000 models/month**; Enterprise/Enterprise+ quote-only with 100,000 models and custom seats . **Free tier**: Yes, 1 developer seat with 3,000 models. **Best for**: teams wanting the dbt ecosystem without self-hosting—**trade-off**: seat costs escalate quickly; initial Enterprise quotes are often 20–40% above final negotiated prices .



- **[Coalesce.io](https://coalesce.io/)**

  **Visual data transformation platform** with column-aware SQL generation. **Pricing**: **Developer (free)** for 1 user with **2,000 actions/month**; **Starter $150/user/month** (annual) for up to 4 transform users with **15,000 actions/month**; Enterprise custom with 100,000 actions . **Free tier**: Yes, 1 user with 2,000 actions. **Best for**: teams wanting a visual canvas over Snowflake, Databricks, or BigQuery—**trade-off**: action-based metering; Starter caps at 4 users, forcing Enterprise for larger teams .



- **[Snowflake Dynamic Tables](https://www.snowflake.com/)**

  **Declarative materialized views** with automatic refresh. **Pricing**: Included with Snowflake credits; **Cloud Services costs scale with active tables and target lag**—a pipeline of 200 tables at 1-minute lag generates ~288,000 change-detection checks daily, potentially exceeding the 10% billing threshold . **Free tier**: Trial credits. **Best for**: Snowflake customers wanting declarative pipelines without external tooling—**trade-off**: short target lag amplifies Cloud Services costs; suspended tables still incur storage fees .



- **[Materialize](https://materialize.com/)**

  **Streaming SQL database** for real-time transformation. **Pricing**: **Cloud On-Demand $1.50/compute credit**; **Cloud Capacity** annual prepaid with volume discounts; **Community License free forever** up to **24 GiB memory and 48 GiB disk** . **Free tier**: Yes, self-managed Community up to 24 GiB. **Best for**: teams needing sub-second freshness on streaming data—**trade-off**: compute credits at $1.50/hour add up for always-on clusters .



- **[Prophecy.io](https://www.prophecy.ai/)**

  **AI-powered data transformation** with visual and code interfaces. **Pricing**: **Starter (free)** with **20 credits/month**; **Professional $150/user/month** with 50 credits; **Enterprise Express $4,000/month** for up to 20 users . **Free tier**: Yes, 20 credits/month. **Best for**: teams wanting AI-assisted pipeline development with Alteryx/Informatica migration—**trade-off**: credit-based AI usage; Enterprise Express at $48K/year is the realistic entry for teams .



- **[Dataform](https://cloud.google.com/dataform)**

  **SQL-based transformation in BigQuery**. **Pricing**: **No license fee**—you pay only for BigQuery compute (**$6.25/TiB on-demand, first 1 TiB free**) and storage (**~$0.023/GiB-month**) . **Free tier**: Yes, 1 TiB BigQuery queries/month. **Best for**: BigQuery-native teams wanting free transformation tooling—**trade-off**: BigQuery-only; no multi-warehouse support .



- **[Matillion](https://www.matillion.com/)**

  **Low-code ETL/ELT** with in-warehouse transformation. **Pricing**: **Credit-based** (~$2/credit per third-party listings); **no public list pricing**—Vendr negotiates 15–25% multi-year discounts . **Free tier**: Trial only. **Best for**: teams doing heavy in-warehouse transformation—**trade-off**: always-on CDC bills by the clock; warehouse compute is a second bill .



- **[Fivetran Transformations](https://www.fivetran.com/)**

  **dbt Core and Quickstart models** within Fivetran. **Pricing**: **First 5,000 successful model runs/month free**; then **$0.01/run (5K–30K)**, **$0.007/run (30K–100K)**, **$0.002/run (100K+)** . **Free tier**: Yes, 5,000 model runs/month. **Best for**: Fivetran customers wanting bundled transformation—**trade-off**: third-party orchestrations (dbt Cloud, Coalesce) are free—you pay only for Fivetran-hosted models .



- **[Databricks Delta Live Tables](https://www.databricks.com/)**

  **Declarative pipeline framework** with expectations. **Pricing**: **DBU premium by edition**—CORE (lowest), PRO (adds CDC), ADVANCED (adds quality expectations); paying for ADVANCED without EXPECT clauses is a silent leak . **Free tier**: Community Edition limited. **Best for**: Databricks customers wanting declarative pipelines with data quality—**trade-off**: edition mismatch wastes premium; serverless background features bill at $0.70–$0.95/DBU vs classic $0.40–$0.55 .



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
