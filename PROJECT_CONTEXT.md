# SITARA — Project Context

## Purpose
SITARA manages Rapim meetings, live minutes, decisions, Decision Briefs, action items, PIC assignments, follow-up monitoring, documents, notifications, and audit history.

## Selected foundation
This workspace uses the engineering starter from `sitara_starter1.zip` as the base: React + TypeScript + Vite, FastAPI, SQLAlchemy 2.x, Alembic, and PostgreSQL. The legacy prototype concepts are preserved separately under `backend/app/models/legacy_prototype.py` for migration planning only.

## Important implementation status
This is a migration workspace, not a complete production application. The starter currently has a health endpoint and placeholder frontend. Business routes, authentication, RBAC, production data models, Alembic migrations, and frontend feature pages still require implementation and tests.

## Source-of-truth rules
1. Inspect current source before changing it.
2. `docs/sitara_schema_v1_draft.sql` is a draft reference, not an applied schema.
3. Do not connect legacy models to the production database until the draft schema and migration strategy are reviewed.
4. Never commit `.env`, local databases, `.venv`, `node_modules`, build artifacts, or real documents.
5. Only claim tests pass when actually run.

## Recommended next steps
1. Verify `.gitignore` and remove generated files from Git tracking safely.
2. Review/normalize the PostgreSQL schema and create initial Alembic migration.
3. Implement auth and server-side RBAC.
4. Implement meetings and live notes.
5. Build decisions and action items from structured meeting data.
6. Add Decision Brief workflow, approvals, progress, documents, notifications, audit log, and reports.
7. Build React pages and API integration in feature slices with tests.
