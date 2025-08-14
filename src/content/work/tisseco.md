---
title: Fleet management system (Tisseco)
publishDate: 2025-01-15 00:00:00
status: in progress
img: /assets/works/tisseco_pav.png
img_alt: Fleet management system (React + NestJS)
description: |
  Fleet management platform for Tisseco, a company engaged in collecting and reselling clothes at low prices, integrating geospatial search, large-scale data imports, and a production-ready NestJS architecture (DDD).
link: ''
tags:
  - NestJS
  - React
technos:
  - TypeScript
  - TypeORM
  - PostgreSQL
  - PostGIS
  - BullMQ
  - Redis
  - JWT
  - MJML
  - Jest
  - E2E (transactional)
  - Docker
  - GitHub Actions
  - Coolify
  - Netdata
  - AWS S3
  - React
  - Vite
  - Tailwind (DaisyUI)
  - Zod
  - TanStack Router
  - TanStack Query
  - TanStack Form
---

## A pragmatic and solid back-end

Tisseco collects and resells second-hand clothes in thrift stores, with a strong environmental and social mission (work reintegration programs).  
The goal: a **management and tracking platform** for their clothing collection containers, providing full traceability, reporting, and a public interface for container lookup and issue reporting.

### Goals

- **Production-ready back-end** with clear DDD boundaries
- Multi-entity tracking: **Sites → Areas → Containers**
- Handling the creation and tracking of **Tours** (to define the "program" a driver must follow)
- Advanced geospatial search (PostGIS)
- Reliable **mass CSV imports** with queueing and reporting
- QR codes for seamless field operations
- Robust deployment and monitoring

### Architecture

- **DDD structure**: `presentation/`, `application/`, `domain/`, `infrastructure/`
- **Persistence**: TypeORM (migrations, seeders)
- **Geospatial**: PostgreSQL **PostGIS** (Haversine, ST_DWithin, polygons)
- **Async processing**: **BullMQ** for heavy tasks (imports, emails)
- **Cache & rate limiting**: Redis with explicit keys and user-scoped cache
- **Mailing**: **MJML** templates
- **Testing**: unit (Jest) + **transactional E2E** (per-test rollback)
- **Observability**: structured logs + **Netdata**
- **Ops**: Docker, Coolify (deploy), GitHub Actions (CI/CD), AWS S3 backups

### Highlights

- Reusable NestJS boilerplate with strict conventions: logging, error handling, `.env` validation, safe caching
- PostGIS search by radius or polygon, with type filters
- CSV import pipeline: staging, validation, queueing (BullMQ), per-row errors, email report
- Cache strategy without “zombie caches” via controlled keys (a problem occuring with redis tags)
- Strong security: guards, roles, per-route & per-user cache control
- Field-friendly UX: QR codes on containers for quick scanning

### Features

- CRUD for sites, areas, containers
- Geospatial search (radius, polygon, type filters)
- High-volume CSV imports with detailed reports
- Auth & roles (JWT), rate limiting, contextual logs
- Transactional emails with MJML templates
- Admin ops: automated deploys, monitoring, S3 backups

### Challenges & learnings

- **Load resilience**: queue-driven imports avoid DB locks & keep UI responsive
- **Business rule isolation**: domain rules are testable without DB
- **Cache safety**: explicit keys & user-scoped decorators prevent bad invalidations
- **Geospatial accuracy**: PostGIS functions are faster & index-friendly

### Tech stack

**Back-end**: NestJS, TypeScript, TypeORM, PostgreSQL + PostGIS, BullMQ, Redis, JWT, MJML  
**Front-end**: React, Vite, Tailwind + DaisyUI  
**Quality**: Jest (unit), transactional E2E tests  
**Ops**: Docker, GitHub Actions, Coolify, Netdata, AWS S3
