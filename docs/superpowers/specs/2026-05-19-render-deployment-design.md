# Spec: Render Deployment for Scrumboy

**Status:** Draft
**Date:** 2026-05-19
**Topic:** Render Deployment Configuration

## 1. Overview
The goal is to enable easy deployment of the Scrumboy Kanban board to Render.com using a Blueprint (`render.yaml`) and providing a detailed Vietnamese guide for a team of 5 users.

## 2. Technical Constraints
- **Platform:** Render (Free Tier)
- **Runtime:** Docker
- **Storage:** Persistent Disk (1GB) for SQLite database.
- **Project Configuration:** 
    - Default SQLite path: `/data/app.db`
    - Environment variable for DB: `SQLITE_PATH`
    - Port: `8080` (exposed in Dockerfile)

## 3. Implementation Details

### 3.1 `render.yaml` (Blueprint)
This file will define the web service and the attached persistent disk.
- **Service Type:** `web`
- **Runtime:** `docker`
- **Plan:** `free`
- **Environment Variables:**
    - `APP_ENV=production`
    - `SQLITE_PATH=/data/app.db`
    - `SCRUMBOY_MODE=full`
- **Disk:**
    - Name: `scrumboy-data`
    - Mount Path: `/data`
    - Size: `1GB`

### 3.2 Deployment Guide (`Huong_dan_trien_khai_Render.md`)
A Vietnamese markdown file containing:
- Prerequisite accounts (GitHub, Render).
- Steps to Fork the repository.
- Steps to create `render.yaml` (if not already present).
- Steps to deploy via Render Dashboard.
- Post-deployment instructions for team setup (Admin registration, inviting members).

## 4. Verification Plan
- Verify `render.yaml` syntax.
- Verify environment variables match `internal/config/config.go`.
- Ensure paths in the guide match the actual file structure.
