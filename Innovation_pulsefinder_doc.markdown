# PulseFinder Documentation (v0.9.0)

## Overview
PulseFinder aggregates trends, initially for fintech markets, but adaptable for creative audience insights or strategic planning.

## Setup
- **Requirements**: Python 3.12, `db_writer.py`.
- **Install**: Place `Innovation_pulsefinder.py` in `H:\DBforISO`.
- **Run**: `python Innovation_pulsefinder.py`.

## Usage
- Input: Market or data list (e.g., `[{'market': 'US', 'users': 1000}]`).
- Action: Calculates trend metrics, logs to `Custom_Tools`.
- Output: Returns metric (e.g., adoption rate).

## Modification for Use Cases
- **Creative (Audience Insights)**:
  ```python
  def audience_insights(self, audience_data):
      engagement = sum(d['views'] for d in audience_data) / len(audience_data) if audience_data else 0
      data = {'Name': 'PulseFinder', 'Description': f'Audience engagement: {engagement:.2f}', 'Status': 'In Progress', 'Fintech_Focus': 'Creative', 'Version': 'v0.9.1'}
      write_to_db('Custom_Tools', data)
      return engagement
  ```
- **Strategic (Innovation Trends)**:
  ```python
  def innovation_trends(self, idea_data):
      adoption = sum(d['adoption'] for d in idea_data) / len(idea_data) if idea_data else 0
      data = {'Name': 'PulseFinder', 'Description': f'Innovation adoption: {adoption:.2f}%', 'Status': 'In Progress', 'Fintech_Focus': 'Strategic', 'Version': 'v0.9.2'}
      write_to_db('Custom_Tools', data)
      return adoption
  ```

## Version History
- **v0.9.0** (May 25, 2025): Prototype, fintech trends.