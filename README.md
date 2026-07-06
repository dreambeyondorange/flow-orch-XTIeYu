# flow-orch-XTIeYu

Profile Epic service.

## Database Migrations

Plain SQL migration files live in `migrations/`. Files follow the `V{NNN}__{description}.sql` naming convention for sequential ordering.

To apply a migration against a local PostgreSQL database:

```sh
psql -v ON_ERROR_STOP=1 -f migrations/V001__create_profiles_table.sql
```

All migrations are idempotent (`CREATE TABLE IF NOT EXISTS`) and safe to run more than once.

**Production:** applying migrations to a production database requires human authorization.
