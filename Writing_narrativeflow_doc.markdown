# NarrativeFlow Documentation (v0.1.0)

## Overview
NarrativeFlow produces narratives, initially for fintech marketing, but adaptable for creative storytelling or strategic communications.

## Setup
- **Requirements**: Python 3.12, `db_writer.py`.
- **Install**: Place `Writing_narrativeflow.py` in `H:\DBforISO`.
- **Run**: `python Writing_narrativeflow.py`.

## Usage
- Input: Campaign list (e.g., `[{'id': 1, 'type': 'Payment Ad'}]`).
- Action: Estimates engagement, logs to `Custom_Tools`.
- Output: Returns engagement percentage.

## Modification for Use Cases
- **Creative (Storytelling)**:
  ```python
  def tell_story(self, campaign_id, theme):
      data = {'Name': 'NarrativeFlow', 'Description': f'Story for campaign {campaign_id}: {theme}', 'Status': 'Planned', 'Fintech_Focus': 'Creative', 'Version': 'v0.1.1'}
      write_to_db('Custom_Tools', data)
      return theme
  ```
- **Strategic (Communications)**:
  ```python
  def strategic_comm(self, campaign_id, message):
      data = {'Name': 'NarrativeFlow', 'Description': f'Communication for campaign {campaign_id}: {message}', 'Status': 'Planned', 'Fintech_Focus': 'Strategic', 'Version': 'v0.1.2'}
      write_to_db('Custom_Tools', data)
      return message
  ```

## Version History
- **v0.1.0** (May 25, 2025): Planned, basic narrative generation.