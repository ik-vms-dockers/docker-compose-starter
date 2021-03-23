# Database Migrations

- [Docs](https://dev.to/drminnaar/flyway---getting-started-3emm)
- [Git Example](https://github.com/drminnaar/flyway/blob/master/README.md)

* V1_1__Create_hero_schema.sql - Creates a new _hero\_data_ schema

  ```sql
  CREATE SCHEMA hero_data AUTHORIZATION postgres;
  ```

* V1_2__Create_hero_table.sql - Create a new _hero_ table in the _hero\_data_ schema

  ```sql
  CREATE TABLE hero_data.hero
  (
      id BIGSERIAL NOT NULL,
      name VARCHAR(250) NOT NULL,
      description TEXT NOT NULL,
      debut_year INT NOT NULL,
      appearances INT NOT NULL,
      special_powers INT NOT NULL,
      cunning INT NOT NULL,
      strength INT NOT NULL,
      technology INT NOT NULL,
      created_at TIMESTAMPTZ NOT NULL,
      updated_at TIMESTAMPTZ NOT NULL
  );

  ALTER TABLE hero_data.hero ADD CONSTRAINT pk_hero_id PRIMARY KEY (id);
  ```
