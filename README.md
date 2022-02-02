# 100 days of data stack

## Day - 1-31-2022
usually people starts about a broad consept of what they wanna do as a plan and they take it from there. I will start with the last 2 steps, i have good idea of what i wanna use for visualization it will be either metabase or apache-superset. So for now i will start with exploring the T from ETL,ELT which is transformation. The tool i will test today is dbt-core which is the open source version of dbt.

## Day - 1-1-2022
after installing dbt i was struggling with running the docs server as it was one of
the features that i was intrested in, there for it did not work saying there is an error
in the configuration where there should be a name for the project that should matches in the profiles.yml file.

[issues]
    [#1]: `dbt run` command is not running 

[solutions]
    [#1]: changing the projetc name in the dbt_project.yml seems to solve the issue. Not sure if it's a conflect with something.

facing another issue when i run dbt run which is asking to setup a database connection in the /home/malnajdi/.dbt/profiles.yml

## Day - 2-1-2022
i have created a database in postgres and user and cofigured /home/malnajdi/.dbt/profiles.yml to have these configurations, now running `dbt run` seems to work and 
it created 1 table and 1 view.

Per the configuration `dbt_project.yml` anything under the models/example will be ran and it will create them as views unless otherwise specified in the model file itself
the variable that will be used is `materialized` if you assign `materialized: view` means it will create the target model as view and `materialized: table` it will create it as table.

