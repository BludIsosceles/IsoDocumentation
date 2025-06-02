# SQLite Database Documentation (v1.0.0)

## Overview
SQLite (`workshop_iso.db`) stores Workshop Iso’s data, supporting fintech, creative, strategic, and operational projects. It’s the core data layer for all tools.

## Setup
- **Requirements**: SQLite3, Python 3.12.
- **Location**: `H:\DBforISO\workshop_iso.db`.
- **Access**: Via `dashboard.py` or `db_writer.py`.

## Usage
- **Tables**: `personnel`, `teams`, `projects`, `Decision`, `Custom_Tools`, `Security_Audits`.
- **Write**: Use `dashboard.py` forms or `db_writer.py`.
- **Query**: `SELECT * FROM Custom_Tools` for tool data.

## Modification for Use Cases
- **Creative (Content Tracking)**:
  ```sql
  CREATE TABLE Content (Content_ID INTEGER PRIMARY KEY, Title TEXT, Views INTEGER);
  ```
- **Strategic (Plan Tracking)**:
  ```sql
  CREATE TABLE Plans (Plan_ID INTEGER PRIMARY KEY, Goal TEXT, Progress REAL);
  ```

## Version History
- **v1.0.0** (May 22, 2025): Initial deployment, core tables.