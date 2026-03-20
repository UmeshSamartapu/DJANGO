Got it 👍 — you want **SQLite (`db.sqlite3`) commands in Django**, structured from **scratch → advanced** in a clean way.

I’ll keep it **simple + practical + project-oriented**.

---

# 🧱 0. Scratch Level (Start SQLite in Django)

| Command                    | Purpose                            |
| -------------------------- | ---------------------------------- |
| `python manage.py migrate` | Creates `db.sqlite3` automatically |
| `sqlite3 db.sqlite3`       | Open SQLite CLI                    |
| `.help`                    | Show all SQLite commands           |
| `.tables`                  | Show all tables                    |
| `.exit`                    | Exit SQLite                        |

👉 First time DB is created when you run:

```bash
python manage.py migrate
```

---

# 🟢 Level 0 (Basic Viewing Data)

| Command                            | Purpose                |
| ---------------------------------- | ---------------------- |
| `.tables`                          | List all tables        |
| `.schema`                          | Show full DB structure |
| `.schema tablename`                | Show table structure   |
| `SELECT * FROM tablename;`         | View all data          |
| `SELECT column FROM tablename;`    | View specific column   |
| `SELECT * FROM tablename LIMIT 5;` | View limited rows      |

👉 Example:

```sql
SELECT * FROM auth_user;
```

---

# 🟢 Beginner Level (Basic CRUD)

| Command                           | Purpose     |
| --------------------------------- | ----------- |
| `INSERT INTO table VALUES (...);` | Add data    |
| `SELECT * FROM table;`            | Read data   |
| `UPDATE table SET col=value;`     | Update data |
| `DELETE FROM table WHERE id=1;`   | Delete data |
| `WHERE`                           | Filter data |
| `ORDER BY col ASC/DESC`           | Sort data   |

👉 Example:

```sql
INSERT INTO myapp_model (name) VALUES ('Umesh');

UPDATE myapp_model SET name='NewName' WHERE id=1;

DELETE FROM myapp_model WHERE id=1;
```

---

# 🟡 Intermediate Level (Query Power 🔥)

| Command                           | Purpose             |
| --------------------------------- | ------------------- |
| `SELECT COUNT(*) FROM table;`     | Count rows          |
| `SELECT DISTINCT col FROM table;` | Unique values       |
| `LIKE '%text%'`                   | Search pattern      |
| `JOIN`                            | Combine tables      |
| `GROUP BY col`                    | Group data          |
| `HAVING`                          | Filter grouped data |
| `ORDER BY`                        | Sorting             |
| `LIMIT`                           | Pagination          |

👉 Example:

```sql
SELECT COUNT(*) FROM auth_user;

SELECT * FROM auth_user WHERE username LIKE '%admin%';

SELECT * FROM table1
JOIN table2 ON table1.id = table2.id;
```

---

# 🔴 Advanced Level (DB Control & Optimization)

| Command                     | Purpose             |
| --------------------------- | ------------------- |
| `CREATE TABLE`              | Create new table    |
| `DROP TABLE table;`         | Delete table        |
| `ALTER TABLE ADD COLUMN`    | Modify table        |
| `CREATE INDEX`              | Improve performance |
| `PRAGMA table_info(table);` | Table details       |
| `PRAGMA database_list;`     | DB info             |
| `VACUUM;`                   | Clean DB            |
| `ANALYZE;`                  | Optimize queries    |
| `.dump`                     | Export full DB      |
| `.read file.sql`            | Import SQL          |

👉 Example:

```sql
CREATE TABLE test (
  id INTEGER PRIMARY KEY,
  name TEXT
);

CREATE INDEX idx_name ON test(name);

VACUUM;
```

---

# ⚡ Django-Specific DB Commands (Important 🔥)

| Command                                | Purpose                |
| -------------------------------------- | ---------------------- |
| `python manage.py dbshell`             | Open SQLite via Django |
| `python manage.py makemigrations`      | Create migration files |
| `python manage.py migrate`             | Apply DB changes       |
| `python manage.py sqlmigrate app 0001` | View SQL               |
| `python manage.py flush`               | Delete all data        |
| `python manage.py dumpdata`            | Export JSON            |
| `python manage.py loaddata`            | Import JSON            |

---

# 🧠 Real Workflow (What You’ll Actually Do Daily)

```bash
# create DB
python manage.py migrate

# open DB
sqlite3 db.sqlite3

# check tables
.tables

# view data
SELECT * FROM myapp_model;

# exit
.exit
```

---

# 🔥 Pro Tips (Very Useful)

✅ SQLite table naming in Django:

```
appname_modelname
```

Example:

```
myapp_irisprediction
```

✅ If error:

```
no such table
```

👉 Run:

```bash
python manage.py makemigrations
python manage.py migrate
```

---
