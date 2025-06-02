# ExperienceCraft Documentation (v0.1.0)

## Overview
ExperienceCraft develops immersive interfaces, initially for fintech payment apps, but adaptable for creative experiences or strategic visualizations.

## Setup
- **Requirements**: Python 3.12, `db_writer.py`.
- **Install**: Place `Interactive Experiences_experiencecraft.py` in `H:\DBforISO`.
- **Run**: `python Interactive Experiences_experiencecraft.py`.

## Usage
- Input: Design list (e.g., `[{'id': 1, 'type': 'Payment UI'}]`).
- Action: Estimates engagement, logs to `Custom_Tools`.
- Output: Returns engagement percentage.

## Modification for Use Cases
- **Creative (Interactive Content)**:
  ```python
  def interactive_content(self, design_id, content):
      data = {'Name': 'ExperienceCraft', 'Description': f'Interactive content for design {design_id}: {content}', 'Status': 'Planned', 'Fintech_Focus': 'Creative', 'Version': 'v0.1.1'}
      write_to_db('Custom_Tools', data)
      return content
  ```
- **Strategic (Visualization)**:
  ```python
  def strategic_viz(self, design_id, data):
      data = {'Name': 'ExperienceCraft', 'Description': f'Strategic viz for design {design_id}: {data}', 'Status': 'Planned', 'Fintech_Focus': 'Strategic', 'Version': 'v0.1.2'}
      write_to_db('Custom_Tools', data)
      return data
  ```

## Version History
- **v0.1.0** (May 25, 2025): Planned, basic interface creation.