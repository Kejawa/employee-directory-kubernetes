# Kubernetes Troubleshooting

## Problem: Employee API Returned HTTP 500

The frontend initially displayed:

```text
GET /api/employees 500 Internal Server Error
```

---
Root Cause
---
The PostgreSQL database was stored on a PersistentVolumeClaim.

The PVC already contained a PostgreSQL data directory, so PostgreSQL reported:

```text
PostgreSQL Database directory appears to contain a database;
Skipping initialization
```

Because the database was already initialized, init.sql was not executed again.

The employees table therefore did not exist.

---
### Lesson
---

Persistent storage survives Pod recreation.

init.sql is an initialization mechanism, not a migration mechanism.

For production applications, database migrations should be used to manage
schema changes over time.