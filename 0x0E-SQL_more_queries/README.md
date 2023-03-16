# SQL - More queries

In this project, I continued to practicing SQL queries, working with
permissoins, joins, and constraints.

## Usage :dolphin:

* Scripts [3-force_name.sql](./3-force_name.sql) forward take the database to query from
as a MySQL command line argument.

```
$ cat 3-force_name.sql | mysql -hlocalhost -uroot -p hbtn_0d_2
```

* Tasks 3-101 query from the database [hbtn_0d_tvshows.sql](./hbtn_0d_tvshows.sql`).
* Tasks 102-103 query from the database [hbtn_0d_tvshows_rate.sql](./hbtn_0d_tvshows_rate.sql).

## Tasks :page_with_curl:

* **0. My privileges!**
  * [0-privileges.sql](./0-privileges.sql): MySQL script that lists all privileges of the users
  `user_0d_1` and `user_0d_2`.

* **1. Root user**
  * [1-create_user.sql](./1-create_user.sql): MySQL script that creates the user `user_0d_1` with
  all privileges and password `user_0d_1_pwd`.

* **2. Read user**
  * [2-create_read_user.sql](./2-create_read_user.sql): MySQL script that creates the database
  `hbtn_0d_2` and user `user_0d_2` with password `user_0d_2_pwd`.
  * `user_0d_2` only has SELECT privilege on the database `hbtn_0d_2`.

* **3. Always a name**
  * [3-force_name.sql](./3-force_name.sql): MySQL script that creates the table `force_name`.
  * Description:
    * `id`: INT
    * `name`: VARCHAR(256) (cannot be null)

* **4. ID can't be null**
  * [4-never_empty.sql](./4-never_empty.sql): MySQL script that creates the table `id_not_null`.
  * Description:
    * `id`: INT (default value = 1)
    * `name`: VARCHAR(256)

* **5. Unique ID**
  * [5-unique_id.sql](./5-unique_id.sql): MySQL script that creates the table `unique_id`.
  * Description:
    * `id`: INT (default value = 1, must be unique)
    * `name`: VARCHAR(256)

* **6. States table**
  * [6-states.sql](./6-states.sql): MySQL script that creates the database `hbtn_0d_usa`
  with a table `states`.
  * `states` description:
    * `id`: INT (unique, auto-generated, cannot be null and is a primary key)
    * `name`: VARCHAR(256) (cannot be null)

* **7. Cities table**
  * [7-cities.sql](./7-cities.sql): MySQL script that creates the database `hbtn_0d_usa`
  with a table `cities`.
  * `cities` description:
    * `id`: INT (unique, auto-generated, cannot be null and is a primary key)
    * `state_id`: INT (cannot be null, foreign key that references to id of the
    `states` table)
    * `name`: VARCHAR(256) (cannot be null)


