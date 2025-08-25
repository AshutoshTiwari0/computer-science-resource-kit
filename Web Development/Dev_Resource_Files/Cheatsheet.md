# Prisma Commands Cheat Sheet

A quick reference for important Prisma CLI commands.

---

## Initialization & Setup
- **`npx prisma init`**  
  Creates a new `prisma/` folder with `schema.prisma` and `.env`.

---

## Database & Migrations
- **`npx prisma migrate dev --name <migration_name>`**  
  Creates and applies a new migration to the database. (Development use)

- **`npx prisma migrate deploy`**  
  Applies all pending migrations to the production database.

- **`npx prisma migrate reset`**  
  Drops the database, recreates it, and reapplies all migrations. (Dev only)

---

## Schema & Client
- **`npx prisma generate`**  
  Generates the Prisma Client from your `schema.prisma`.  
  Run after editing schema.

- **`npx prisma db push`**  
  Pushes schema changes directly to the database **without migrations**. (Prototype/early dev)

- **`npx prisma db pull`**  
  Introspects an existing database and updates `schema.prisma`.

---

## Studio & Tools
- **`npx prisma studio`**  
  Opens Prisma Studio (a GUI to manage your DB).

- **`npx prisma format`**  
  Formats `schema.prisma`.

---

## Debugging & Maintenance
- **`npx prisma validate`**  
  Validates the `schema.prisma`.

- **`npx prisma version`**  
  Shows Prisma CLI & Engine versions.

---

## Typical Workflow
```bash
# 1. Initialize Prisma
npx prisma init

# 2. Make schema changes & migrate
npx prisma migrate dev --name init

# 3. Generate Prisma Client
npx prisma generate

# 4. Open Prisma Studio (optional)
npx prisma studio
