This folder contains SQL scripts for initializing the PostgreSQL database used by the project.

schema.sql
- Creates `users` table and inserts seed data (Alice, Bob, Charlie).

How to import (local PostgreSQL):
1. Start PostgreSQL (install if needed).
2. Create a database:
   createdb go_echo_db
3. Import schema:
   psql -d go_echo_db -f db/schema.sql

Connection details (example):
- Host: localhost
- Port: 5432
- DB: go_echo_db
- User: your_postgres_user
- Password: your_password

Next steps for the Go app:
- Add a Postgres connection using `database/sql` and `github.com/lib/pq` or `github.com/jackc/pgx`.
- Replace in-memory `users` slice with DB queries.
