# PromptMaster Documentation (v0.9.0)

## Overview
PromptMaster is an AI tool for analytics, initially for fintech payment data, but adaptable for creative content analytics, strategic forecasting, or operational metrics.

## Setup
- **Requirements**: Python 3.12, `db_writer.py`.
- **Install**: Place `AI Prompt Engineering_promptmaster.py` in `H:\DBforISO`.
- **Run**: `python AI Prompt Engineering_promptmaster.py`.

## Usage
- Input: Transaction or data list (e.g., `[{'id': 1, 'amount': 100}]`).
- Action: Calculates metrics, logs to `Custom_Tools`.
- Output: Returns metric (e.g., conversion rate).

## Modification for Use Cases
- **Creative (Content Engagement)**:
  ```python
  def analyze_content(self, content_data):
      engagement = sum(d['views'] for d in content_data) / len(content_data) if content_data else 0
      data = {'Name': 'PromptMaster', 'Description': f'Content engagement: {engagement:.2f}', 'Status': 'In Progress', 'Fintech_Focus': 'Creative', 'Version': 'v0.9.1'}
      write_to_db('Custom_Tools', data)
      return engagement
  ```
- **Strategic (Market Forecasting)**:
  ```python
  def forecast_trends(self, market_data):
      growth = sum(d['growth'] for d in market_data) / len(market_data) if market_data else 0
      data = {'Name': 'PromptMaster', 'Description': f'Market growth: {growth:.2f}%', 'Status': 'In Progress', 'Fintech_Focus': 'Strategic', 'Version': 'v0.9.2'}
      write_to_db('Custom_Tools', data)
      return growth
  ```

## Version History
- **v0.9.0** (May 25, 2025): Prototype, fintech analytics.