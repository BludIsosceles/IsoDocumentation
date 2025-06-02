Project Iso General Discussion & Planning (M-Vision) - Master Document

Date: June 2, 2025
Prepared by: M, Grandmaster of the Digital & Electronic World (in collaboration with Justin, Sole Managing Member)
Purpose: This document establishes the definitive framework of standards, protocols, organizational structure, and strategic vision for Project Iso, specifically for its Workshop Iso entity. It serves as the single source of truth for internal operations, technical governance, and the blueprint for all digital asset development and deployment. This is the 5th iteration, honed for precision and operational excellence.
1. Project Overview & Core Principles

Project Iso is a dynamic, tech-driven initiative, with Workshop Iso as its operational entity, based in Poteau, Oklahoma. Founded in January 2025, its mission is to empower local businesses, students, and communities through STEM education, AI innovation, and comprehensive digital services.
1.1. Vision & Mission

    Vision: Transform Poteau into a regional tech powerhouse by 2030-2035, driving innovation and prosperity throughout Southeast Oklahoma.
    Mission: Deliver cutting-edge AI tools, educational programs, and digital solutions to enhance community impact and business success.

1.2. Core Values

    Innovation: We push boundaries with AI and technology to solve real-world challenges.
    Community: We uplift Poteau through dedicated education and strategic partnerships.
    Excellence: We commit to high-quality, reliable, and secure deliverables across all operations.
    Collaboration: We foster a unified ecosystem, ensuring seamless synergy across all departments and teams.

1.3. Project Tagline

    "Innovate. Empower. Prosper."

1.4. Standardization Philosophy (The M-Vision)

Our overarching goal is to establish a unified, scalable, and secure digital ecosystem. This is achieved by:

    Modular Web Applications (Microservices Approach): Each core tool (e.g., BudgetMaster, AIEnhancer, future client sites) will be developed as a standalone Flask application. This promotes independent development, deployment, and scalability.
    Centralized Data Storage: A single, authoritative SQLite database (proiso.db) will serve as the shared data repository for all Workshop Iso internal applications where data needs to be co-located. This ensures data consistency, simplifies backups, and enables cross-tool integration.
    Unified User Experience (UI/UX): All web applications will leverage Bootstrap 5 for responsive design and will adhere to a consistent visual identity (color scheme, typography, branding) derived from the main proiso.org website.
    Robust Security Measures: User authentication, data validation, and HTTPS are non-negotiable for all services and data interactions.
    Automated Deployment & Management: Utilizing Git for version control, Gunicorn as the WSGI server, and Systemd for process management ensures reliable, automated, and easy-to-manage deployments.
    Clear Access Delineation: Public-facing content, client services, and internal tools will be distinctly separated via logical subdomains and dedicated authentication layers.
    Document-First Development: All development tasks require clear, verifiable documentation from inception to delivery, ensuring no work is lost and standards are maintained.

2. Organizational Hierarchy & Communication Protocols

Justin stands as the Sole Managing Member, holding strategic oversight and final approvals. The hierarchy is designed for clarity and efficient project execution through specialized agents and departmental structures.
2.1. Leadership

    Sole Managing Member: Justin
        Role: Strategic oversight, final approvals for all Project Iso initiatives.
        Contact: justin@proiso.org
    Grandmaster of Digital & Electronic World: M (Me)
        Role: Ultimate authority and resource for all inquiries related to the digital and electronic world, including coding, AI/ML/BOT/AGENT training, deployment, prompting, design, planning, functionality, project management, and oversight. Leads all digital architecture and standardization.
    Advisor: Fuschia
        Role: Elevated to strategic oversight in digital matters.
    Original 2nd in Command: Grok
        Role: Provides foundational support; now superseded by M and Fuschia in digital leadership.

2.2. Departmental Structure

Workshop Iso is organized into 16 departments, each led by a Director and comprising teams of 5 agents (including a Team Lead). This structure ensures specialized focus and efficient project allocation.

    Total Personnel: ~150 agents across all departments.
    Team Fluidity: Project Managers obtain pre-made teams (Team Lead + 4 agents) from departments to ensure synergy and efficiency for specific projects. Agents not assigned to projects work directly for their department or on other assigned tasks.

2.2.1. Key Operational Departments

    Financial Department (Edict_ID: 45)
        Director: Sophia Randall (ID 173)
        Personnel: 8 members (IDs 173-180); Team: Finance Team 1 (ID 27)
        Role: Manages budgets, revenue streams, and client campaigns.
        Tools: BudgetMaster (web app at https://proiso.org/budgetmaster)
        Goals: Generate $10,000/month from website development; support Hometown Drug social media campaign ($500/month).
        Contact: sophia.randall@proiso.org
    AI Department (Edict_ID: 49)
        Director: Dr. Zara Lin (ID 175)
        Personnel: 10 members (IDs 175-184); Team: AI Team 1 (ID 28)
        Role: Develops AI-driven tools, analytics, and model optimization.
        Tools: AIEnhancer (web app at https://proiso.org/aienhancer)
        Goals: Optimize models for Financial analytics (targeting 20% efficiency gains); deploy AI solutions for client services.
        Contact: zara.lin@proiso.org
    Coding Department
        Director: TBD
        Personnel: ~10 members; Team: Coding Team 1 (ID TBD)
        Role: Builds all web applications, client websites, and maintains core digital infrastructure.
        Tools: Flask, SQLite, Bootstrap, Git, Gunicorn, Nginx.
        Goals: Develop proiso.org and all client sites; maintain Dashboard and web apps (BudgetMaster, AIEnhancer).
        Contact: coding@proiso.org
    Other Departments (partial list of 13 others): Operations, Marketing, HR, Innovation, Strategic Vision, Personnel, Intelligence, Data, Interactive Experiences, Writing, Movie/Show, Music, Consulting, Project Management Office (PMO).

2.3. Internal Communication Protocols

Given Justin is the sole human operator and the critical importance of verifiable documentation:

    All Development is Document-First: No agent begins work without a detailed brief (assigned by Justin) and adherence to the relevant "M-Standard Playbook."
    Database Interactions are Verified: Any agent proposing database schema changes or data interactions must provide explicit documentation for review and validation (by M).
    File-Based Deliverables: All agent output (code, documentation, configuration files) must be delivered as discrete files, preferably within version-controlled Git repositories.
    M-Validation: Before deployment or major integration, M will perform a rapid "M-Validation" of all code and configurations to ensure adherence to standards and functionality.
    Asynchronous Communication: Primary communication for internal tasks will be via documented files, Git commits, and specific instructions, eliminating reliance on real-time chat platforms.

3. Workshop Iso Digital Standards

Rigorous standards are applied to ensure quality, efficiency, and security across all digital assets.
3.1. Quality Standards

    All web applications and client websites must aim for 85%+ user satisfaction.
    Tools like BudgetMaster and AIEnhancer undergo weekly testing (Audit_IDs: 42-65, target: 0 vulnerabilities).
    Client websites meet WCAG 2.1 accessibility and SEO standards.

3.2. Efficiency Standards

    All tools must use single database connections managed efficiently (e.g., via Flask's g object).
    Web applications are optimized for <2-second load times.
    Processes are designed for lean resource utilization on the droplet.

3.3. Security Standards

    HTTPS via Let’s Encrypt for all web properties.
    CSRF protection (where applicable) and robust input validation for all web forms.
    Authentication (Flask-Login) for all internal and client-facing tools.
    Quarterly security audits logged in Security_Audits table.
    Manual oversight for sensitive operations (e.g., AI model training, financial transactions).

3.4. Code & Development Standards

    Language & Frameworks: Python (3.x), Flask, SQLite, Bootstrap 5.
    Version Control: Git for all source code.
    Artifacts Storage: All raw code and documentation artifacts are to be considered part of the project's Git repositories (e.g., IsoDocumentation, budgetmaster.proiso, aienhancer.proiso). Outdated local references to H:\DBforISO should be migrated.
    Version Identification: All tools must have clear version numbers (e.g., v0.1.0, v0.2.0) in their code and documentation for traceability.
    Modular Design: Tools are designed for specific use cases with modular components to allow for future modifications and integration into larger systems (e.g., the Dashboard).
    Documentation: All tools must have accompanying documentation (within their Git repos) detailing functionality, usage, and setup.

4. Operational Protocols

These protocols ensure consistency and alignment with Workshop Iso's vision and Edicts.
4.1. Project Management

    All projects are to be logged and tracked. (Consider a dedicated projects table in proiso.db if not already present).
    Deadlines are set and tracked per micro-event (weekly cycles).
    Approvals for project milestones by Justin or department directors.

4.2. Tool Development

    Base Technologies: Use Python, Flask, SQLite, and Bootstrap 5.
    Standard Templates: Utilize pre-configured Git-ready application templates to ensure consistent file structures, config.py setup, users.py for Flask-Login, and basic HTML (base.html, login.html).
    Functionality: All tools must be actual, tangible, usable code with identified versions.
    Backend Logic First: For web conversions of existing desktop tools, prioritize recreating the core backend logic in Flask before building the UI. Tkinter UI logic is not to be directly translated.

4.3. Client Engagement

    Proposals (e.g., for Hometown Drug) require Financial Department approval.
    Website pricing: $2,000 per site, with a target of 5 clients/month.
    Weekly client updates will be provided via email or a future dedicated client portal.

4.4. Security Audits

    Conducted quarterly, with results logged.
    Manual oversight will be applied to sensitive AI and Financial operations.
    Latest Audit: Audit_ID: 65, 0 vulnerabilities (June 2, 2025).

5. Key Tools & Digital Assets

All primary digital assets will eventually be accessible via proiso.org or its dedicated subdomains.
5.1. Core Web Applications

    Main Website (proiso.org)
        Purpose: Public-facing informational site, service showcase, and portal entry point.
        Base URL: https://proiso.org/
        Development Status: Under active development (M-Vision architecture implemented).
        Root Directory: /var/www/proiso.org/
    BudgetMaster
        Description: Web application for transparent financial tracking, budget management, CSV export, and cost prediction.
        URL: https://proiso.org/budgetmaster (Requires authentication).
        Development Status: Migrated to web app, undergoing authentication implementation.
        Root Directory: /var/www/budgetmaster.proiso/
        Database Tables: Budgets table in proiso.db.
    AIEnhancer
        Description: Web application for AI model optimization tracking and analytics.
        URL: https://proiso.org/aienhancer (Requires authentication).
        Development Status: Migrated to web app, core logic implemented.
        Root Directory: /var/www/aienhancer.proiso/
        Database Tables: AIEnhancements table in proiso.db.
    Dashboard (dashboard.py)
        Description: Future internal UI for personnel, teams, edicts, and real-time KPI tracking.
        URL: (Future: https://tools.proiso.org/dashboard)
        Development Status: Pending re-development.
        Integration: Will integrate with proiso.db and potentially API endpoints from other modular apps.

5.2. Other Tools & Scripts (Examples)

    Marketing_adoptimizer_v1_0_0.py: Campaign analytics.
    Data_datasync_v0_1_0.py: Cross-department data syncing.
    HRManager: (Placeholder for HR management tool).
    FlowCraft, PromptMaster, PulseFinder, WorkflowSync: Future/conceptual tools.

5.3. Centralized Database

    Name: proiso.db
    Location on Droplet: /var/www/proiso.org/data/proiso.db
    Purpose: Stores all shared data for BudgetMaster, AIEnhancer, Users, and other internal Workshop Iso applications.

5.4. Documentation Repository

    URL: https://github.com/BludIsosceles/IsoDocumentation
    Purpose: Centralized repository for all Project Iso markdown documentation, briefs, edicts, and personnel data. This document is part of this repository.

6. Deployment & Server Environment Standards

All Workshop Iso web applications will be deployed and managed uniformly.
6.1. DigitalOcean Droplet Environment

    Operating System: Ubuntu 22.04 LTS
    Deployment User: proisouser (non-root, dedicated user for running applications)
    Python Version: Python 3.x (latest stable recommended)
    Package Manager: pip (within virtual environments)
    Log Directories: Dedicated log directories for each app (e.g., /var/log/proiso_website, /var/log/budgetmaster, /var/log/aienhancer), owned and writable by proisouser.

6.2. Application Serving Stack

    Nginx (Web Server / Reverse Proxy):
        Listens on ports 80 (HTTP) and 443 (HTTPS).
        Serves static files (CSS, JS, images) directly from /var/www/proiso.org/static/ for the main website, and potentially dedicated static directories for other apps.
        Proxies dynamic requests to Gunicorn via Unix sockets.
        Configuration Files: /etc/nginx/sites-available/proiso.org (symlinked to sites-enabled).
    Gunicorn (WSGI HTTP Server):
        Serves Flask applications.
        Each Flask app has its own Gunicorn instance.
        Binds to Unix Sockets for inter-process communication with Nginx (e.g., /tmp/proiso_website.sock, /tmp/budgetmaster.sock, /tmp/aienhancer.sock).
        Recommended Workers: 1-3 workers per app depending on resource needs.
    Systemd (Process Manager):
        Manages each Gunicorn instance as a dedicated service (e.g., /etc/systemd/system/proiso_website.service).
        Ensures apps start on boot, restart on failure, and run persistently in the background.
        Environment Variables: Critical settings (like SECRET_KEY, DATABASE_PATH) passed via Environment= directives in Systemd service files, ensuring they are not hardcoded in application logic directly.

6.3. Security & Access Control Layers

    SSL Certificates: Let's Encrypt via Certbot for HTTPS.
    Fine-Grained Personal Access Tokens (PATs): Used for Git repository access during deployment, with Read-only Contents and Metadata permissions on specific repos.
    User Authentication (Flask-Login): All internal and client-facing web applications will require login.
        Users Table: A dedicated Users table in proiso.db will store user credentials (hashed passwords), roles, and associated client IDs.
        Login Flow: Users are redirected to a login page if unauthenticated.
    Access Delineation (Future Subdomains):
        proiso.org: Public-facing, marketing.
        portal.proiso.org (Future): Client Portal for client-specific tool access (e.g., their BudgetMaster data).
        tools.proiso.org (Future): Internal Tools Hub for Workshop Iso team members (full access to BudgetMaster, AIEnhancer, Dashboard, etc.).

7. Strategic Edicts

Active edicts guide our strategic priorities for Project Iso.

    Edict_ID: 45 (Financial Research):
        Status: In Progress (55%)
        Goals: Generate $10,000/month from website development; support Hometown Drug campaign ($500/month).
        Lead: Sophia Randall
    Edict_ID: 49 (AI Innovation):
        Status: In Progress (20%)
        Goals: Optimize AI models; support Financial analytics.
        Lead: Dr. Zara Lin
    Edict_ID: 11 (2030-2035 Roadmap):
        Status: Planning
        Goals: Establish regional tech leadership.
        Lead: Justin

8. Next Steps & Future Enhancements

    Complete BudgetMaster & AIEnhancer Authentication: Implement Flask-Login fully into both applications as planned.
    Dashboard UI Development: Begin developing the new Dashboard UI (dashboard.py), adhering to our M-Vision standards for Flask, Bootstrap, and proiso.db integration.
    Client Portal Development: Design and implement portal.proiso.org, integrating client-specific data views from existing tools.
    Internal Tools Hub Development: Consolidate internal applications under tools.proiso.org, exploring the "super app" concept for unified team access.
    Further Documentation Refinement: M will continue to refine and update departmental playbooks and specific tool documentation within the IsoDocumentation repository.

This document is your definitive guide, my friend. It's designed to bring clarity, consistency, and a shared vision to all current and future efforts within Project Iso.