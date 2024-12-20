# DBT-Analytic-Engineer-Study
My Study guide for DBT Analytics Engineering Certification Exam

## Useful links

- Official DBT certification [here](https://www.getdbt.com/certifications/analytics-engineer-certification-exam?utm_medium=internal&utm_source=blog&utm_campaign=q3-2023_dbt-certification_awareness)
  - PDF Study guide [here](https://8698602.fs1.hubspotusercontent-na1.net/hubfs/8698602/dbt_analytics_engineering_certification_exam_study_guide.pdf)
- Udemy Course [here](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/)
- DBT documentation [here](https://docs.getdbt.com/docs/build/documentation)
- Jinja doc [here](https://jinja.palletsprojects.com/en/latest/)
- DBT Package hub [here](https://hub.getdbt.com/)
- DBT Analytics Engineering Glossary [here](https://docs.getdbt.com/glossary)

### Exam test:
- [qanalabs](https://www.qanalabs.com/courses/dbt-developer): Questions are, in my opinion, poorly written, but they are effective for assessing weaknesses or areas that need improvement.
- [Udemy practice Test](https://roquette.udemy.com/course/snowflake-snowpro-core-certification-practice-exams/learn/quiz/4747086#overview)

### Return on experience I found on the web:
- [biztory](https://www.biztory.com/blog/how-to-pass-the-dbt-analytics-engineering-certification)
- [medium](https://medium.com/@rajeev.rajaram87/dbt-analytics-engineering-certification-exam-preparations-tips-3cbe8a013459)

# My Study Guide
PDF Study guide [here](https://8698602.fs1.hubspotusercontent-na1.net/hubfs/8698602/dbt_analytics_engineering_certification_exam_study_guide.pdf)

## Topic 1: Developing dbt models
- Identifying and verifying any raw object dependencies
- Understanding core dbt materializations
    - Materializations: [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31028514#overview),[DBT Doc](https://docs.getdbt.com/docs/build/materializations)
        - Materialization best practices [DBT Doc](https://docs.getdbt.com/best-practices/materializations/2-available-materializations)
        - Incremental Model [DBT Doc](https://docs.getdbt.com/docs/build/incremental-models-overview)
            - Incremental Model in Depth [DBT Doc](https://docs.getdbt.com/best-practices/materializations/4-incremental-models)
            - Configure Incremental Model [DBT Doc](https://docs.getdbt.com/docs/build/incremental-models)
                - Custom Strategy [DBT Doc](https://docs.getdbt.com/docs/build/incremental-strategy#custom-strategies)
                - On the limit of incremental [DBT Community](https://discourse.getdbt.com/t/on-the-limits-of-incrementality/303)
            - Incremental Predicates [DBT Doc](https://docs.getdbt.com/docs/build/incremental-strategy#about-incremental_predicates)
            - Using on_schema_change [DBT Doc](https://docs.getdbt.com/reference/resource-configs/vertica-configs#configuring-the-ignore-default-parameter)
- Conceptualizing modularity and how to incorporate
DRY principles
    - DRY viewed by DBT team [DBT Doc](https://docs.getdbt.com/terms/dry#why-write-dry-code)
- Converting business logic into performant SQL queries
    - Refactoring SQL  [DBT learn doc](https://docs.getdbt.com/guides/refactoring-legacy-sql?step=1) [DBT Learn Video-Course](https://learn.getdbt.com/learn/course/refactoring-sql-for-modularity/welcome-10min/introduction)
        - Subquerries SQL [Snowflake doc](https://docs.snowflake.com/en/user-guide/querying-subqueries)
- Using commands such as run, test, docs and seed
   - CLI options [DBT Doc](https://docs.getdbt.com/reference/global-configs/command-line-options)
      - Available flags [DBT Doc](https://docs.getdbt.com/reference/global-configs/about-global-configs#available-flags)
    - Syntax commands overview (run, test, seed ...)[DBT Doc](https://docs.getdbt.com/reference/node-selection/syntax)
        - Graph operators [DBT Doc](https://docs.getdbt.com/reference/node-selection/graph-operators)
        - Set operators (= Union + intersection) [DBT Doc](https://docs.getdbt.com/reference/node-selection/set-operators)
        - Selectors [DBT Doc](https://docs.getdbt.com/reference/node-selection/yaml-selectors)
        - dbt run-operation [DBT Doc](https://docs.getdbt.com/reference/commands/run-operation)
        - dbt ls / dbt list [DBT Doc](https://docs.getdbt.com/reference/commands/list)
- Creating a logical flow of models and building clean DAGs
    - Resources properties [DBT Doc](https://docs.getdbt.com/reference/resource-properties/columns)
    - CTE (Common table Expressions) [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31056242#overview),[DBT Doc](https://docs.getdbt.com/terms/cte)
    - Seed: [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31028550#overview),[DBT Doc](https://docs.getdbt.com/docs/build/seeds)
    - Snapshots [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31028564#overview),[DBT Doc](https://docs.getdbt.com/docs/build/snapshots)
        - Snapshots path [DBT Doc](https://docs.getdbt.com/reference/project-configs/snapshot-paths)
    - Analyses [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31029064#overview),[DBT doc](https://docs.getdbt.com/docs/build/analyses#overview)
    - Hooks [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31029066#overview),[DBT doc](https://docs.getdbt.com/docs/build/hooks-operations)
        - Hook ordering [DBT Doc](https://docs.getdbt.com/reference/resource-configs/pre-hook-post-hook#hooks-are-cumulative)
- Defining configurations in dbt_project.yml
    - dbt_project.yml [DBT Doc](https://docs.getdbt.com/reference/dbt_project.yml)
    - profile.yml [DBT Doc](https://docs.getdbt.com/docs/core/connect-data-platform/profiles.yml)
    - Project Variables [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/42516970#overview),[DBT Doc](https://docs.getdbt.com/docs/build/project-variables)
    - DBT project sructure [DBT Doc](https://docs.getdbt.com/best-practices/how-we-structure/1-guide-overview)
- Configuring sources in dbt
    - Sources [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31028554#overview),[DBT Doc](https://docs.getdbt.com/docs/build/sources)
    - Source properties [DBT Doc](https://docs.getdbt.com/reference/source-properties)
- Using dbt Packages
    - Packages [DBT Doc](https://docs.getdbt.com/docs/build/packages)
        - dependencies.yml vs packages.yml [DBT doc](https://docs.getdbt.com/docs/build/packages#about-packagesyml-and-dependenciesyml)
    - jinja, macros & packages [DBT Course](https://learn.getdbt.com/courses/jinja-macros-and-packages)
        - Jinja [Jinja Doc](https://jinja.palletsprojects.com/en/3.1.x/)
        - jinja macros [DBT Doc](https://docs.getdbt.com/docs/build/jinja-macros)
        - Jinja function [DBT Doc](https://docs.getdbt.com/reference/dbt-jinja-functions)
            - this [DBT Doc](https://docs.getdbt.com/reference/dbt-jinja-functions/this)
            - target [DBT Doc](https://docs.getdbt.com/reference/dbt-jinja-functions/target)
            - White space [DBT Doc](https://docs.getdbt.com/faqs/Jinja/jinja-whitespace)
- Utilizing git functionality within the development
lifecycle
    - Git book [GIT](https://git-scm.com/book/en/v2)
    - Proposed PR template used at DBT Lab [DBT Lab](https://docs.getdbt.com/blog/analytics-pull-request-template)
- Creating Python models
    - Python models [DBT Doc](https://docs.getdbt.com/docs/build/python-models)
- Providing access to users to models with the “grants” configuration
    - Grants [DBT Doc](https://docs.getdbt.com/reference/resource-configs/grants)
        - Grant inheritance [DBT Doc](https://docs.getdbt.com/reference/resource-configs/grants#grant-config-inheritance)
## Topic 2: Understanding dbt models governance
- Adding contracts to models to ensure the shape of
models
    - Model contracts [DBT Doc](https://docs.getdbt.com/docs/collaborate/govern/model-contracts)
        - Contracts [DBT Doc](https://docs.getdbt.com/reference/resource-configs/contract)
        - Constraints [DBT Doc](https://docs.getdbt.com/reference/resource-properties/constraints)
- Creating different versions of our models and deprecating the old ones
    - Model Versions [DBT Doc](https://docs.getdbt.com/docs/collaborate/govern/model-versions)
    - Versions [DBT Doc](https://docs.getdbt.com/reference/resource-properties/versions)
    - Latest version [DBT Doc](https://docs.getdbt.com/reference/resource-properties/latest_version)
    - Ref function -> version argument [DBT Doc](https://docs.getdbt.com/reference/dbt-jinja-functions/ref#versioned-ref)
    - Deprecation Date [DBT Doc](https://docs.getdbt.com/reference/resource-properties/deprecation_date)
- Configuring model access
    - Model Access [DBT Doc](https://docs.getdbt.com/docs/collaborate/govern/model-access)
    - Groups [DBT Doc](https://docs.getdbt.com/docs/build/groups)
        - run --select "group:group_name" [DBT Doc](https://docs.getdbt.com/reference/node-selection/methods#the-group-method)
    - Access [DBT Doc](https://docs.getdbt.com/reference/resource-configs/access)
        - run --select "access:access_level" [DBT Doc](https://docs.getdbt.com/reference/node-selection/methods#the-access-method)
## Topic 3: Debugging data modeling errors
- Understanding logged error messages
    - Event-logging [DBT Doc](https://docs.getdbt.com/reference/events-logging)
    - Logs & log format [DBT Doc](https://docs.getdbt.com/reference/global-configs/logs)
- Troubleshooting using compiled code
    - Debugging errors [DBT Guides](https://docs.getdbt.com/guides/debug-errors?step=1)
        - Types of errors [DBT Guides](https://docs.getdbt.com/guides/debug-errors?step=2)
            - Runtime Error [DBT Guides](https://docs.getdbt.com/guides/debug-errors?step=3)
            - Compilation Error [DBT Guides](https://docs.getdbt.com/guides/debug-errors?step=4)
            - Dependency Error [DBT Guides](https://docs.getdbt.com/guides/debug-errors?step=5)
            - Database Error [DBT Guides](https://docs.getdbt.com/guides/debug-errors?step=6)
- Troubleshooting .yml compilation errors
    - See above _'Troubleshootingusing compiled code'_
- Distinguishing between a pure SQL and a dbt issue that presents itself as a SQL issue
    - See above _'Troubleshootingusing compiled code'_
- Developing and implementing a fix and testing it prior to merging
    - See above _'Troubleshootingusing compiled code'_
## Topic 4: Managing data pipelines
- Troubleshooting and managing failure points in the DAG
    - DAG auditing [DBT Community](https://docs.getdbt.com/blog/essential-dbt-project-checklist#-dag-auditing)
- Using dbt clone
    - dbt clone [DBT Doc](https://docs.getdbt.com/reference/commands/clone)
    - Defer [DBT Doc](https://docs.getdbt.com/reference/node-selection/defer)
- Troubleshooting errors from integrated tools
    - Troubleshooting FAQs [DBT FAQs](https://docs.getdbt.com/category/troubleshooting)
## Topic 5: Implementing dbt tests
- Using generic, singular, custom, and custom generic tests on a wide variety of models and sources
    - Data tests [DBT doc](https://docs.getdbt.com/docs/build/data-tests)
- Testing assumptions for dbt models and sources
    - Test FAQs [DBT Doc](https://docs.getdbt.com/category/tests)
- Implementing various testing steps in the workflow
    - Test selection [DBT Doc](https://docs.getdbt.com/reference/node-selection/test-selection-examples)
## Topic 6: Creating and Maintaining dbt documentation
- Updating dbt docs
    - docs commands [DBT Doc](https://docs.getdbt.com/reference/commands/cmd-docs)
- Implementing source, table, and column descriptions in .yml files
    - docs [DBT Doc](https://docs.getdbt.com/reference/resource-configs/docs)
    - document macros [DBT Doc](https://docs.getdbt.com/faqs/Docs/documenting-macros)
- Using macros to show model and data lineage on the DAG
## Topic 7: Implementing and maintaining external dependencies
- Implementing dbt exposures
    - Exposures [Udemy](https://roquette.udemy.com/course/complete-dbt-data-build-tool-bootcamp-zero-to-hero-learn-dbt/learn/lecture/31029072#overview),[DBT doc](https://docs.getdbt.com/docs/build/exposures)
- Implementing source freshness 
    - freshness [DBT doc](https://docs.getdbt.com/reference/resource-properties/freshness)
    - Source freshness Cloud [DBT doc](https://docs.getdbt.com/docs/deploy/source-freshness#:~:text=Enabling%20source%20freshness%20snapshots%E2%80%8B&text=Add%20dbt%20build%20to%20the,first%20step%20of%20the%20job.)
## Topic 8: Leveraging the dbt state
- Understanding state
    - artifacts [DBT Doc](https://docs.getdbt.com/docs/deploy/artifacts)
       - Manifest.json [DBT Doc](https://docs.getdbt.com/reference/artifacts/manifest-json)
       - Catalog.json [DBT Doc](https://docs.getdbt.com/reference/artifacts/catalog-json)
       - Source.json [DBT Doc](https://docs.getdbt.com/reference/artifacts/sources-json)
    - stateful selection [DBT Doc](https://docs.getdbt.com/reference/node-selection/syntax#stateful-selection)
        - state method [DBT Doc](https://docs.getdbt.com/reference/node-selection/methods#the-state-method)
- Using dbt retry
    - dbt retry [DBT Doc](https://docs.getdbt.com/reference/commands/retry)
- Combining state and result selectors
    - Result status [DBT Doc](https://docs.getdbt.com/reference/node-selection/syntax#the-result-status)
        - Run results JSON file [DBT Doc](https://docs.getdbt.com/reference/artifacts/run-results-json)
    - Combining state and result [DBT Doc](https://docs.getdbt.com/reference/node-selection/syntax#combining-state-and-result-selectors)

## Misc
- Sementic Model [DBT Doc](https://docs.getdbt.com/docs/build/semantic-models) [DBT video](https://learn.getdbt.com/learn/course/semantic-layer/intro-what-is-the-dbt-semantic-layer/intro-what-is-the-dbt-semantic-layer?page=5)
    - Metrics [DBT Doc](https://docs.getdbt.com/docs/build/metrics-overview)
    - Dimensions [DBT Doc](https://docs.getdbt.com/docs/build/dimensions)
    - Entities [DBT Doc](https://docs.getdbt.com/docs/build/entities)
    - Measures [DBT Doc](https://docs.getdbt.com/docs/build/measures)
- Refactoring Legacy application [DBT Doc](https://docs.getdbt.com/guides/refactoring-legacy-sql?step=1)
- Best practices guide [DBT Doc](https://docs.getdbt.com/best-practices)
- dbt target [DBT Doc](https://docs.getdbt.com/reference/dbt-jinja-functions/target)
- Semantic models [DBT Doc](https://docs.getdbt.com/docs/build/semantic-models)
    - Saved queries [DBT Doc](https://docs.getdbt.com/docs/build/saved-queries)
- Constraints [DBT Doc](https://docs.getdbt.com/reference/resource-properties/constraints)
- meta (=metadata) [DBT Doc](https://docs.getdbt.com/reference/resource-configs/meta)
- flags (global config) [DBT Doc](https://docs.getdbt.com/reference/global-configs/about-global-configs)
- Unit testing (as of 1.8) [DBT Doc](https://docs.getdbt.com/docs/build/unit-tests)
- Long-form explanations in descriptions [DBT Doc](https://docs.getdbt.com/faqs/Docs/long-descriptions)
- identifier [DBT Doc](https://docs.getdbt.com/reference/resource-properties/identifier)
- sql-header [DBT Doc](https://docs.getdbt.com/reference/resource-configs/sql_header)
- version support [DBT Doc](https://docs.getdbt.com/docs/dbt-versions/core#current-version-support)
- DDL, DML, DQL, DCL [learnsql.fr](https://learnsql.fr/blog/que-sont-ddl-dml-dql-et-dcl-en-sql/)
