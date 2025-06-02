# Workshop Iso Personnel and Teams Roster (v1.0.0)

## Overview
This roster contains 121 personnel and 29 teams across 16 departments, supporting Workshop Iso’s diverse project requests (creative, strategic, operational, technical, financial). It’s stored in `H:\DBforISO\workshop_iso.db` (`personnel` and `teams` tables) and accessible via `dashboard.py` Personnel and Teams tabs.

## Departments and Teams
- **Development & Coding** (18 personnel, 3 teams):
  - Team 1: Jerry (Lead), Alice, Bob, Clara, Dave
  - Team 2: Eve (Lead), Frank, Grace, Hank, Ivy
  - Team 3: Jack (Lead), Kara, Liam, Mia, Nate
  - Redundancy: Oscar, Pam (Software Developers), Quinn (QA Tester)
- **Innovation & Strategy** (12 personnel, 2 teams):
  - Team 1: Dr. Lena Kim (Lead), Alan, Beth, Carl, Dana
  - Team 2: Eli (Lead), Fiona, Gus, Holly, Ian
  - Redundancy: Jill (AI Specialist), Kyle (Research Analyst)
- **Operations & Efficiency** (12 personnel, 2 teams):
  - Team 1: Marcus Lee (Lead), Nina, Oscar, Pam, Quinn
  - Team 2: Rachel (Lead), Sam, Tina, Uma, Victor
  - Redundancy: Wendy (Workflow Manager), Xander (Logistics Coordinator)
- **Strategic Vision** (10 personnel, 2 teams):
  - Team 1: Nina Patel (Lead), Yara, Zane, Ava
  - Team 2: Ben (Lead), Cara, Dan, Ella
  - Redundancy: Finn (KPI Analyst), Gina (Dashboard Developer)
- **Personnel** (6 personnel, 1 team):
  - Team 1: Sarah Connor (Lead), Hank, Ivy, Jack, Kara
  - Redundancy: Liam (Onboarding Specialist)
- **HR** (6 personnel, 1 team):
  - Team 1: David Kim (Lead), Mia, Nate, Oscar, Pam
  - Redundancy: Quinn (Training Coordinator)
- **Intelligence** (10 personnel, 2 teams):
  - Team 1: Marcus Reed (Lead), Rachel, Sam, Tina
  - Team 2: Uma (Lead), Victor, Wendy, Xander
  - Redundancy: Yara (Cybersecurity Analyst), Zane (Security Engineer)
- **Data** (12 personnel, 2 teams):
  - Team 1: Dr. Emily Zhang (Lead), Alan, Beth, Carl, Dana
  - Team 2: Eli (Lead), Fiona, Gus, Holly, Ian
  - Redundancy: Jill (Database Administrator), Kyle (Data Integrity Specialist)
- **Interactive Experiences** (12 personnel, 2 teams):
  - Team 1: Alex Rivera (Lead), Mia, Nate, Oscar, Pam
  - Team 2: Quinn (Lead), Rachel, Sam, Tina, Uma
  - Redundancy: Victor (Programmer), Wendy (Artist)
- **Writing** (6 personnel, 1 team):
  - Team 1: Sophia Chen (Lead), Xander, Yara, Zane, Ava
  - Redundancy: Ben (Writer)
- **Marketing & Influence** (12 personnel, 2 teams):
  - Team 1: Michael Thompson (Lead), Cara, Dan, Ella, Finn
  - Team 2: Gina (Lead), Hank, Ivy, Jack, Kara
  - Redundancy: Liam (Market Researcher), Mia (Campaign Manager)
- **Movie/Show** (12 personnel, 2 teams):
  - Team 1: Ava DuVernay (Lead), Nate, Oscar, Pam, Quinn
  - Team 2: Rachel (Lead), Sam, Tina, Uma, Victor
  - Redundancy: Wendy (Screenwriter), Xander (Cinematographer)
- **Music** (12 personnel, 2 teams):
  - Team 1: Quincy Jones (Lead), Yara, Zane, Ava, Ben
  - Team 2: Cara (Lead), Dan, Ella, Finn, Gina
  - Redundancy: Hank (Songwriter), Ivy (Musician)
- **Consulting** (6 personnel, 1 team):
  - Team 1: Elon Musk (Lead), Jack, Kara, Liam, Mia
  - Redundancy: Nate (Marketing Consultant)
- **Financial** (6 personnel, 1 team):
  - Team 1: Christine Lagarde (Lead), Oscar, Pam, Quinn, Rachel
  - Redundancy: Sam (Fintech Innovator)
- **PMO** (6 personnel, 1 team):
  - Team 1: Jane Doe (Lead), Tina, Uma, Victor, Wendy
  - Redundancy: Xander (Junior Project Manager)

## Setup
- **Database**: `H:\DBforISO\workshop_iso.db`.
- **Populate**: Run `Other_populate_personnel_teams.py` (`python Other_populate_personnel_teams.py`).
- **View**: Use `dashboard.py` Personnel and Teams tabs or query:
  ```sql
  SELECT * FROM personnel ORDER BY department, team_id;
  SELECT * FROM teams;
  ```

## Usage
- **Projects**: Assign teams (e.g., Jerry’s Coding Team 1) to projects via Project Manager. Teams remain intact for efficiency.
- **Department Operations**: Redundancy personnel (e.g., Oscar in Coding) maintain tasks during team deployments.
- **Modifications**: Add/update via `dashboard.py` (Top Echelon only) or custom scripts.

## Version History
- **v1.0.0** (May 25, 2025): Initial roster, 121 personnel, 29 teams.