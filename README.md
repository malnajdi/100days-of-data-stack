# 100 days of data stack

I have always wanted to build a `data stack`, i had envisioned how it will look like but i wanted to explor the up-to-date stacks and 
see what kind of tech is emerging currently.

For my critera it's:

- Support: OpenSource: Must have a Good Community. Enterprise: well we know how it is.
- Diversity: Won't limit my options in terms of integration `in or out` if something is not support i should be able to build it my self.
- Usability: A team with different backgrounds shall have an easy time to operate it.
- Open Source First.

Some tools to keep in mind:

- Metabase
- Apache-Superset


## Day - 1-31-2022
Usually people starts about a broad consept of what they wanna do as a plan and they take it from there. I will start with the last 2 steps, 
i have good idea of what i wanna use for visualization it will be either metabase or apache-superset. So for now i will start with exploring 
the T from ETL,ELT which is transformation. The tool i will test today is dbt-core which is the open source version of dbt.


## Day - 2-1-2022
after installing dbt i was struggling with running the docs server as it was one of
the features that i was intrested in, there for it did not work saying there is an error
in the configuration where there should be a name for the project that should matches in the profiles.yml file.

Issues:
- #1: `dbt run` command is not running 

Solutions
- #1: changing the projetc name in the dbt_project.yml seems to solve the issue. Not sure if it's a conflect with something.

facing another issue when i run dbt run which is asking to setup a database connection in the /home/malnajdi/.dbt/profiles.yml


## Day - 2-2-2022
i have created a database in postgres and user and cofigured /home/malnajdi/.dbt/profiles.yml to have these configurations, now running `dbt run` seems to work and 
it created 1 table and 1 view.

Per the configuration `dbt_project.yml` anything under the models/example will be ran and it will create them as views unless otherwise specified in the model file itself
the variable that will be used is `materialized` if you assign `materialized: view` means it will create the target model as view and `materialized: table` it will create it as table.

## Day - 2-3-2022

I tried to test the Extract and Loading data Intro a Warehouse, I used the tool called airbyte. Still
testing and playing with it. It has a docker-compose https://github.com/airbytehq/airbyte.

## Day - 2-4-2022

break


