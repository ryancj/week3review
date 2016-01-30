#SQL and Sinatra Review
This week, we are going to review some SQL concepts, and some web concepts,
using Sinatra.

Let's start out by creating a new directory, and initializing a git repository.

## SQL Review
[SQLZoo](www.sqlzoo.net) | [SQLFiddle](www.sqlfiddle.com)

Let's start out by [creating a database](http://www.postgresql.org/docs/9.3/static/app-createdb.html)
with a table called members.
```sql
CREATE TABLE members (
  id SERIAL PRIMARY KEY,
  email_address VARCHAR(50) NOT NULL,
  password VARCHAR(50) NOT NULL
  );

  INSERT INTO members (email_address, password) VALUES ('drew@codecore.ca','123'),
  ('drew_two@codecore.ca','123'), ('drew_three@codecore.ca','123'),
  ('drew_four@codecore.ca','123'), ('drew_five@codecore.ca','123')
```
Now, query the table for all members whose id is greater than two.
```sql
SELECT * FROM members WHERE id > 2;
```
