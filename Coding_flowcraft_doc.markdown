# FlowCraft Documentation (v1.0.0)

## Overview
FlowCraft is a UI framework for Workshop Iso’s dashboards, powering `dashboard.py`. It supports fintech payment displays and is adaptable for creative, strategic, or operational UIs.

## Setup
- **Requirements**: Python 3.12, Tkinter, `db_writer.py`.
- **Install**: Place `Coding_flowcraft.py` in `H:\DBforISO`.
- **Run**: `python Coding_flowcraft.py`.

## Usage
- Launch: Opens a Tkinter window with a "Log Payment Display" button.
- Action: Logs display events to `Custom_Tools`.
- Output: Confirms via messagebox.

## Modification for Use Cases
- **Creative (Movie/Show UI)**:
  ```python
  def log_content_display(self, content_id):
      data = {'Name': 'FlowCraft', 'Description': f'Content display for {content_id}', 'Status': 'Deployed', 'Fintech_Focus': 'Creative', 'Version': 'v1.0.1'}
      write_to_db('Custom_Tools', data)
  ```
- **Strategic (Planning Dashboard)**:
  ```python
  def log_strategy_view(self, plan_id):
      data = {'Name': 'FlowCraft', 'Description': f'Strategy view for plan {plan_id}', 'Status': 'Deployed', 'Fintech_Focus': 'Strategic', 'Version': 'v1.0.2'}
      write_to_db('Custom_Tools', data)
  ```

## Version History
- **v1.0.0** (May 22, 2025): Initial release, fintech focus.