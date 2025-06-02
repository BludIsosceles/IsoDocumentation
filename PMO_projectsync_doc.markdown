# ProjectSync Documentation (v0.1.0)

## Overview
ProjectSync coordinates projects, initially for fintech, but adaptable for creative or strategic initiatives.

## Setup
- **Requirements**: Python 3.12, `db_writer.py`.
- **Install**: Place `PMO_projectsync.py` in `H:\DBforISO`.
- **Run**: `python PMO_projectsync.py`.

## Usage
- Input: Task list (e.g., `[{'id': 1, 'task': 'Creative Video'}]`).
- Action: Estimates completion, logs to `Custom_Tools`.
- Output: Returns completion percentage.

## Modification for Use Cases
- **Creative (Video Project)**:
  ```python
  def video_project(self, task_id, milestone):
      data = {'Name': 'ProjectSync', 'Description': f'Video project task {task_id}: {milestone}', 'Status': 'Planned', 'Fintech_Focus': 'Creative', 'Version': 'v0.1.1'}
      write_to_db('Custom_Tools', data)
      return milestone
  ```
- **Strategic (Plan Coordination)**:
  ```python
  def plan_coordination(self, task_id, goal):
      data = {'Name': 'ProjectSync', 'Description': f'Strategic task {task_id}: {goal}', 'Status': 'Planned', 'Fintech_Focus': 'Strategic', 'Version': 'v0.1.2'}
      write_to_db('Custom_Tools', data)
      return goal
  ```

## Version History
- **v0.1.0** (May 25, 2025): Planned, basic project coordination.