# Workshop IsoPro Standards, Protocols, Departments, and Vision

**Date**: June 2, 2025  
**Prepared by**: Justin, Sole Managing Member, Workshop IsoPro  
**Purpose**: Establish a comprehensive framework of standards, protocols, organizational structure, and vision for Workshop IsoPro, serving as a guiding document for internal operations, governance, and external communications, including website development.

## Vision and Mission
Workshop IsoPro is a tech-driven startup in Poteau, Oklahoma, founded in January 2025 to empower local businesses, students, and communities through STEM education, AI innovation, and digital services. Our vision is to become Southeast Oklahoma’s leading tech hub by 2030, fostering economic growth and technological advancement.

- **Vision**: Transform Poteau into a regional tech powerhouse by 2030-2035, driving innovation and prosperity.
- **Mission**: Deliver cutting-edge AI tools, educational programs, and digital solutions to enhance community impact and business success.
- **Core Values**:
  - **Innovation**: Push boundaries with AI and tech solutions.
  - **Community**: Uplift Poteau through education and partnerships.
  - **Excellence**: Commit to high-quality, reliable deliverables.
  - **Collaboration**: Foster a unified ecosystem across departments.
- **Tagline**: “Innovate. Empower. Prosper.”

## Organizational Structure
Workshop IsoPro operates as a collaborative ecosystem with **16 departments**, each led by a director and supported by specialized teams. Below are key departments relevant to our standards and protocols, with a focus on those driving Edict_ID: 45 (Financial Research) and Edict_ID: 49 (AI Innovation).

### Key Departments
1. **Financial Department** (Edict_ID: 45)
   - **Director**: Sophia Randall (ID 173)
   - **Personnel**: 8 members (IDs 173-180)
   - **Team**: Finance Team 1 (ID 27)
   - **Role**: Manages budgets, revenue streams, and client campaigns.
   - **Tools**: `BudgetMaster` (web app at `https://proiso.org/budgetmaster`)
   - **Goals**:
     - Generate $10,000/month from website development (e.g., Hometown Drug, Fort Smith Coffee Co.).
     - Support Hometown Drug’s social media campaign ($500/month).
   - **Contact**: sophia.randall@proiso.org
2. **AI Department** (Edict_ID: 49)
   - **Director**: Dr. Zara Lin (ID 175)
   - **Personnel**: 10 members (IDs 175-184)
   - **Team**: AI Team 1 (ID 28)
   - **Role**: Develops AI-driven tools and analytics.
   - **Tools**: `AIEnhancer` (web app at `https://proiso.org/aienhancer`)
   - **Goals**:
     - Optimize models for Financial analytics (20% efficiency gains).
     - Deploy AI solutions for client services.
   - **Contact**: zara.lin@proiso.org
3. **Coding Department**
   - **Director**: TBD
   - **Personnel**: ~10 members (IDs TBD)
   - **Team**: Coding Team 1 (ID TBD)
   - **Role**: Builds web apps and client websites.
   - **Tools**: Flask, SQLite (`workshop_iso.db`), Bootstrap
   - **Goals**:
     - Develop `proiso.org` and client sites.
     - Maintain `dashboard.py` and web apps.
   - **Contact**: coding@proiso.org
4. **Other Departments** (13 total, partial list):
   - **Operations**: Oversees logistics and workflows.
   - **Marketing**: Manages campaigns (e.g., `Marketing_adoptimizer_v1_0_0.py`).
   - **HR**: Handles personnel (e.g., `HRManager`).
   - **Total Personnel**: ~150 across all departments.

### Leadership
- **Sole Managing Member**: Justin
  - Role: Strategic oversight, final approvals.
  - Contact: justin@proiso.org
- **Key Directors**:
  - Sophia Randall (Financial)
  - Dr. Zara Lin (AI)
  - TBD (Coding, others)

## Standards
Workshop IsoPro adheres to rigorous standards to ensure quality, security, and efficiency across operations.

- **Quality**:
  - All deliverables (e.g., web apps, websites) must achieve 85%+ user satisfaction.
  - Tools like `BudgetMaster` and `AIEnhancer` undergo weekly testing (Audit_IDs: 42-65, 0 vulnerabilities).
  - Client websites meet WCAG 2.1 accessibility and SEO standards.
- **Efficiency**:
  - Tools use single database connections (e.g., `/var/www/workshop_iso.db`).
  - Processes optimized for <2-second response times (e.g., web app load times).
  - Weekly micro-events track progress (e.g., Edict_ID: 45 at 55% completion).
- **Security**:
  - HTTPS via Let’s Encrypt for all web properties.
  - CSRF protection and input validation for web apps.
  - Quarterly security audits (manual oversight for sensitive threads).
- **Collaboration**:
  - Cross-departmental syncing via `Data_datasync_v0_1_0.py`.
  - Weekly updates in Slack threads (Financial, AI, Coding).
  - Real-time KPI dashboard (`dashboard.py`) for ROI and engagement.

## Protocols
Operational protocols ensure consistency and alignment with our vision.

- **Project Management**:
  - All projects logged in `workshop_iso.db` (`projects` table).
  - Deadlines set per micro-event (weekly cycles).
  - Approvals by Justin or department directors via `dashboard.py`.
- **Tool Development**:
  - Use Python, Flask, SQLite, and Bootstrap.
  - Artifacts stored in `H:\DBforISO\artifacts` (e.g., `Financial_budgetmaster_web_v0_2_0.py`).
  - Version control via incremental naming (e.g., `v0_2_0`).
- **Client Engagement**:
  - Proposals (e.g., `Financial_social_media_pitch_hometown_drug_v2.md`) approved by Financial.
  - Websites priced at $2,000 each, 5 clients/month.
  - Weekly client updates via email or portal (`proiso.org`).
- **Security Audits**:
  - Conducted quarterly, logged in `Security_Audits` table.
  - Manual oversight for AI and Financial threads.
  - Latest: Audit_ID: 65, 0 vulnerabilities (June 2, 2025).
- **Communication**:
  - Slack for internal threads (Financial, AI, Coding).
  - Email for client communication (`contact@proiso.org`).
  - Weekly director meetings (chaired by Justin).

## Key Tools and Artifacts
- **BudgetMaster** (`Financial_budgetmaster_web_v0_2_0.py`):
  - Web app for budget tracking, CSV export, and cost prediction.
  - URL: `https://proiso.org/budgetmaster` (pending DNS).
  - Database: `Budgets` table in `workshop_iso.db`.
- **AIEnhancer** (`AIEnhancer_web_v0_1_0.py`):
  - Web app for AI model optimization.
  - URL: `https://proiso.org/aienhancer` (pending DNS).
  - Database: `AIEnhancements` table.
- **Dashboard** (`dashboard.py`):
  - Internal UI for personnel, teams, and edicts.
  - Artifacts tab tracks files in `H:\DBforISO\artifacts`.
- **Other Tools**:
  - `Marketing_adoptimizer_v1_0_0.py`: Campaign analytics.
  - `Data_datasync_v0_1_0.py`: Cross-department syncing.
- **Artifacts** (in `H:\DBforISO\artifacts`):
  - `Financial_social_media_pitch_hometown_drug_v2.md`
  - `Financial_diverse_revenue_streams_poteau_20250525_v3.md`
  - `AI_strategic_plan.md`
  - `Workshop_IsoPro_Website_Development_Brief.md`

## Edicts
Active edicts guide our strategic priorities:

- **Edict_ID: 45 (Financial Research)**:
  - **Status**: In Progress (55%)
  - **Goals**: Generate $10,000/month from website development, support Hometown Drug campaign ($500/month).
  - **Lead**: Sophia Randall
- **Edict_ID: 49 (AI Innovation)**:
  - **Status**: In Progress (20%)
  - **Goals**: Optimize AI models, support Financial analytics.
  - **Lead**: Dr. Zara Lin
- **Edict_ID: 11 (2030-2035 Roadmap)**:
  - **Status**: Planning
  - **Goals**: Establish regional tech leadership.
  - **Lead**: Justin

## Governance
- **Decision-Making**:
  - Justin holds final approval for strategic decisions.
  - Department directors approve operational tasks.
  - Weekly reviews via `dashboard.py` Edicts tab.
- **Resource Allocation**:
  - Budgets managed via `BudgetMaster`.
  - Personnel assigned via `HRManager` or `dashboard.py`.
- **Compliance**:
  - Adhere to local regulations (Poteau, OK).
  - Regular audits ensure data security and quality.

## Contact Information
- **General**: contact@proiso.org
- **Financial**: sophia.randall@proiso.org
- **AI**: zara.lin@proiso.org
- **Coding**: coding@proiso.org
- **Phone**: (918) 555-1234 (confirm actual number)
- **Address**: Poteau, OK 74953 (confirm exact address)

## Next Steps
- **Internal Use**: Share with department directors for alignment.
- **Website Development**: Provide to Coding team or external developer alongside `Workshop_IsoPro_Website_Development_Brief.md`.
- **Updates**: Log changes in `dashboard.py`, update `workshop_iso.db`.