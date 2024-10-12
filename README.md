# My Batis Migration

## About
A repository created while learning [Batis Migrations](https://mybatis.org/migrations/index.html)

## Steps

* Run a [docker postgres instance](https://github.com/gerardnico/postgres)
* Run the `downloadDependencies` [gradle task](build.gradle) or put the PostgresDriver in the [Drivers](drivers) directory
* Install MyBatis
```bash
sdk install mybatis
```
* Run it
```bash
migrate --help
```

## Note on the Repository 

A myBatis repository base directory contains three subdirectories as follows:
* [./drivers](drivers) The loaded drivers
* [./environments](./environments) env `.properties` file 
  * default: `development` is specified in [development.properties](environments/development.properties)
  * The env is specified with the `--env=<environment>` option (without the path and `.properties` part).
* [./scripts](./scripts) contains migration SQL files
  * the [migration script to create the changelog table](scripts/20241012142721_create_changelog.sql), 
  * plus one [empty "first" migration script](scripts/20241012142722_first_migration.sql)


