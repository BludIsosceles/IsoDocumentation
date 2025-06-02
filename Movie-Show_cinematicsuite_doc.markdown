# CinematicSuite Documentation (v0.1.0)

## Overview
CinematicSuite produces videos, initially for fintech promotions, but adaptable for creative storytelling or strategic campaigns.

## Setup
- **Requirements**: Python 3.12, `db_writer.py`.
- **Install**: Place `Movie-Show_cinematicsuite.py` in `H:\DBforISO`.
- **Run**: `python Movie-Show_cinematicsuite.py`.

## Usage
- Input: Script list (e.g., `[{'id': 1, 'type': 'Payment Promo'}]`).
- Action: Estimates engagement, logs to `Custom_Tools`.
- Output: Returns engagement percentage.

## Modification for Use Cases
- **Creative (Storytelling)**:
  ```python
  def story_video(self, script_id, theme):
      data = {'Name': 'CinematicSuite', 'Description': f'Story video for script {script_id}: {theme}', 'Status': 'Planned', 'Fintech_Focus': 'Creative', 'Version': 'v0.1.1'}
      write_to_db('Custom_Tools', data)
      return theme
  ```
- **Strategic (Campaign Video)**:
  ```python
  def campaign_video(self, script_id, goal):
      data = {'Name': 'CinematicSuite', 'Description': f'Campaign video for script {script_id}: {goal}', 'Status': 'Planned', 'Fintech_Focus': 'Strategic', 'Version': 'v0.1.2'}
      write_to_db('Custom_Tools', data)
      return goal
  ```

## Version History
- **v0.1.0** (May 25, 2025): Planned, basic video production.