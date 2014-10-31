---
tags: sql, creating tables, introductory, micro
languages: sql
resources: 
---

# Sql Create Tables Lab

Building off of what we've learned about creating tables and column types in the SQL Book, let's play around with writing SQL CREATE statements.

## Learning Objectives

1. Learn to write SQL CREATE statements
2. Learn about the different column types supported in SQL and SQLite3

## About this Lab

Let's take a look at this lab's structure, which will seem slightly different than what you've been working with before.

```bash
├── bin
│   ├── environment.rb # loads dependencies via Bundler
│   ├── run.rb # runs sql_runner.rb
│   └── sql_runner.rb # a ruby class that handles creating a database connection and executing your SQL files
├── lib
│   └── create_table.sql # where you'll be writing your CREATE statement
└── spec
    ├── spec_helper.rb
    └── create_table_spec.rb # the spec for this lab
```

The way SQL labs work is that you'll write your SQL statements in `.sql` files in the `lib/` directory, and the `run.rb` file in `bin/` will execute them using the `sql_runner.rb` class. When you run the tests, the SQLRunner class is called and a new database is created in memory for the tests.

## Todo

Create a table called cats with the following columns and types:

|column | type  |
|-------|-------|
|id     |primary key|
|name   |text   |
|age    |integer|
|gender |char(1)(The choices would be "M" or "F")|
|breed  |text   |
|temperment|text|
|declawed |boolean|