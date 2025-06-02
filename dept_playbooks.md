Financial Department: M-Standard Playbook

Date: June 2, 2025
Prepared by: M, Grandmaster of the Digital & Electronic World
Purpose: This playbook outlines the technical standards, protocols, and best practices for the Financial Department of Workshop Iso, ensuring seamless integration with the overall Project Iso digital architecture and maximizing efficiency, accuracy, and security in financial operations and client revenue generation.
1. Department Mission & Role

The Financial Department, led by Director Sophia Randall (ID 173), is responsible for managing all budgets, revenue streams, and client campaigns. It drives Workshop Iso's financial health and ensures accurate tracking and reporting of all monetary flows.

    Key Goals:
        Generate $10,000/month from website development initiatives.
        Support specific client campaigns, such as Hometown Drug's social media campaign ($500/month).
        Maintain transparent and auditable financial records.

2. Key Tools & Technologies

The Financial Department's digital operations will primarily leverage:

    BudgetMaster: The core web application for budget tracking, CSV export, and cost prediction (https://proiso.org/budgetmaster).
    AIEnhancer (Indirectly): While primarily an AI Department tool, its analytics capabilities will be crucial for optimizing financial strategies (Edict_ID: 49 support).
    proiso.db (SQLite Database): The central data repository for all budget records and user authentication.
    Dashboard (dashboard.py): Future internal UI for overall project tracking and financial KPIs.
    Python: For scripting and data analysis.
    Pandas & NumPy: For efficient data manipulation and numerical operations (especially within BudgetMaster's prediction model).
    Scikit-learn: For machine learning capabilities, particularly cost prediction in BudgetMaster.
    Git: For version control of any departmental scripts or documentation.

3. Code Quality & Best Practices (for Departmental Scripts/Tools)

Any specialized scripts or data analysis tools developed by the Financial Department must adhere to the following:

    Python (PEP 8): All Python code must strictly follow PEP 8 style guidelines for readability and consistency.
        Naming Conventions: Clear, descriptive names for variables, functions, and classes (e.g., calculate_roi, monthly_revenue_report).
        Docstrings: All functions, classes, and modules must have clear docstrings explaining their purpose, arguments, and return values.
        Comments: Use comments to explain complex logic or non-obvious design choices.
    Database Interaction Protocol:
        Centralized DB: All database operations must target the central proiso.db located at /var/www/proiso.org/data/proiso.db.
        Connection Management: Utilize Flask's g object for database connections (as demonstrated in BudgetMaster's app.py) for efficient and safe connection handling.
        Parameterized Queries: Absolutely critical: Always use parameterized queries (? placeholders) to prevent SQL injection vulnerabilities. Never concatenate user input directly into SQL strings.
        Error Handling: Implement robust try...except sqlite3.Error blocks for all database operations, logging errors (to /var/log/budgetmaster/app.log or similar dedicated log for other scripts) and providing informative feedback.
    Data Validation: All financial inputs (amounts, categories) must be rigorously validated (e.g., numerical checks, positive values, string sanitation) before processing or storage.
    Modularity: Break down complex tasks into smaller, reusable functions or modules. This facilitates auditing, testing, and potential integration into the future Dashboard.
    Efficiency: Optimize data processing for performance, especially when dealing with large datasets or recurring reports.

4. Integration Points

The Financial Department's tools and data integrate directly with the central proiso.db and the broader Project Iso ecosystem.

    proiso.db - Tables of Interest:
        Budgets: Primary table for all budget entries (used by BudgetMaster).
        AIEnhancements: (Read-only access) Provides insights into AI model performance for strategic financial decisions.
        Users: (Read-only for user information, write access for Financial/Admin to manage certain user roles if applicable).
        Future tables (e.g., Projects, Clients, Invoices) will also reside here, adhering to defined schemas.
    BudgetMaster API (Future): As BudgetMaster evolves, it may expose API endpoints for the Dashboard or other tools to programmatically access budget data, reducing direct database dependency.
    Dashboard (dashboard.py): Will pull financial KPIs and project progress data from proiso.db for centralized visualization and reporting.

5. Deployment & Documentation Protocol

All code developed by the Financial Department that requires deployment (e.g., updates to BudgetMaster or new web-enabled tools) will follow the Project Iso standard.

    Version Control: All source code must reside in a dedicated Git repository (e.g., budgetmaster.proiso). Changes are committed and pushed to GitHub regularly.
    Documentation Requirement:
        Every script, tool, or significant code module must have accompanying documentation.
        Documentation (Markdown format preferred) will be stored in the tool's respective Git repository (e.g., budgetmaster.proiso/README.md) and/or referenced in the central IsoDocumentation repository (https://github.com/BludIsosceles/IsoDocumentation).
        Documentation must clearly state:
            Tool's purpose and functionality.
            Dependencies (Python libraries, external APIs).
            Usage instructions.
            Input/output formats.
            Version history.
        No un-documented work will be considered complete or acceptable for deployment.
    Deployment Flow (Reference Master Document):
        Changes pushed to GitHub.
        Pulled onto DigitalOcean Droplet (/var/www/budgetmaster.proiso/).
        Managed by Gunicorn via Systemd service (budgetmaster.service).
        Accessed via Nginx reverse proxy (https://proiso.org/budgetmaster).
    Directives for New Tool Development:
        Any new web-enabled tool must adhere to the Flask/Bootstrap 5/SQLite stack.
        Utilize provided standard application templates to ensure consistent file structures, config.py setup, and users.py for Flask-Login integration.

6. Financial Data Security

Given the sensitive nature of financial data, adherence to security protocols is paramount.

    Authentication: Access to BudgetMaster and any other financial tools requires successful user authentication via Flask-Login.
    Role-Based Access (Future): Implement role-based access control (RBAC) to ensure only authorized personnel can view or modify specific financial data (e.g., only "financial" or "admin" roles can add/edit budgets).
    Data Integrity: Validate all data inputs to prevent corruption or erroneous entries.
    Regular Backups: Ensure that proiso.db backups are routinely performed (currently handled via DigitalOcean Droplet backups).

7. Contact & Support

For technical queries regarding the BudgetMaster application, database integration, or deployment, consult the Coding Department Lead and/or M (Grandmaster of Digital & Electronic World) via Justin.

Sophia Randall (Director, Financial Dept.) is the primary contact for operational and business requirements.
AI Department: M-Standard Playbook

Date: June 2, 2025
Prepared by: M, Grandmaster of the Digital & Electronic World
Purpose: This playbook defines the technical standards, protocols, and best practices for the AI Department of Workshop Iso, ensuring cutting-edge AI innovation, efficient model deployment, and seamless integration with the overall Project Iso digital architecture.
1. Department Mission & Role

The AI Department, led by Director Dr. Zara Lin (ID 175), is responsible for developing, optimizing, and deploying AI-driven tools and analytical solutions for internal use and client services. It drives technological advancement and provides critical insights.

    Key Goals:
        Develop and deploy AI solutions for clients (e.g., AIEnhancer for model optimization).
        Optimize models for Financial analytics, targeting 20% efficiency gains (Edict_ID: 49 support).
        Showcase AI capabilities to attract partnerships.

2. Key Tools & Technologies

The AI Department's digital operations will primarily leverage:

    AIEnhancer: The core web application for tracking AI model optimizations (https://proiso.org/aienhancer).
    proiso.db (SQLite Database): The central data repository for all optimization records and user authentication.
    Dashboard (dashboard.py): Future internal UI for overall project tracking and AI performance KPIs.
    Python: The primary language for AI model development, data processing, and scripting.
    Machine Learning Frameworks: Libraries like TensorFlow, PyTorch, Scikit-learn, etc., for model building and training.
    Pandas & NumPy: For efficient data preparation, manipulation, and numerical operations crucial for AI workflows.
    Git: For version control of all model code, optimization scripts, and documentation.

3. Code Quality & Best Practices (for AI Models & Scripts)

All AI models, optimization scripts, and data pipelines developed by the AI Department must adhere to the following:

    Python (PEP 8): Strict adherence to PEP 8 for readability and maintainability.
        Naming Conventions: Clear, descriptive names for all components (e.g., train_model, predict_sentiment, data_preprocessing_pipeline).
        Docstrings: Comprehensive docstrings for all functions, classes, and modules, detailing purpose, algorithms, arguments, and return values.
        Comments: Use comments to explain complex mathematical logic, algorithmic choices, or non-obvious aspects of AI models.
    Database Interaction Protocol:
        Centralized DB: All database operations must target the central proiso.db located at /var/www/proiso.org/data/proiso.db.
        Connection Management: Utilize Flask's g object for database connections (as demonstrated in AIEnhancer's app.py) for efficient and safe handling.
        Parameterized Queries: Absolutely critical: Always use parameterized queries to prevent SQL injection vulnerabilities.
        Error Handling: Implement robust try...except sqlite3.Error blocks for database interactions, logging errors (to /var/log/aienhancer/app.log or similar dedicated log for other scripts) and providing informative feedback.
    Model Versioning: Beyond code versioning, implement a strategy for versioning trained AI models themselves. Store model artifacts (e.g., .h5, .pkl, .pt files) in a designated, version-controlled location. AIEnhancer should track which model version was optimized.
    Experiment Tracking: For significant model training or optimization runs, record key parameters, metrics, and chosen algorithms (potentially in proiso.db or dedicated experiment tracking tools) to ensure reproducibility.
    Modularity: Separate model definition, training logic, evaluation, and deployment interfaces into distinct modules or functions.
    Performance Optimization: Given the emphasis on "optimization" (Edict_ID: 49), strive for efficiency in model training, inference, and resource usage.

4. Integration Points

The AI Department's tools and data integrate directly with the central proiso.db and the broader Project Iso ecosystem.

    proiso.db - Tables of Interest:
        AIEnhancements: Primary table for tracking AI model optimization efforts (used by AIEnhancer).
        Budgets: (Read-only access) For understanding financial context influencing AI project resource allocation.
        Users: (Read-only access) For user information if AI tools have user-specific features.
        Future tables (e.g., Model_Artifacts, Experiment_Runs) will reside here.
    AIEnhancer API (Future): AIEnhancer is envisioned to expose API endpoints for the Dashboard or other tools to trigger optimizations programmatically or fetch optimization data programmatically.
    Financial Department Support: Provide optimized models or analytical insights to the Financial Department for their Edict_ID: 45 goals.

5. Deployment & Documentation Protocol

All code and models developed by the AI Department that require deployment (e.g., updates to AIEnhancer, new web-enabled AI tools, or deployed inference services) will follow the Project Iso standard.

    Version Control: All source code and non-large model artifacts must reside in a dedicated Git repository (e.g., aienhancer.proiso). Changes are committed and pushed to GitHub regularly.
    Documentation Requirement:
        Every script, tool, or significant code module (including trained models) must have accompanying documentation.
        Documentation (Markdown format preferred) will be stored in the tool's respective Git repository and/or referenced in the central IsoDocumentation repository.
        Documentation must clearly state:
            Tool/Model purpose, functionality, and algorithmic approach.
            Dependencies (Python libraries, ML frameworks, data sources).
            Usage/Inference instructions.
            Training data sources and preprocessing steps.
            Evaluation metrics and performance benchmarks.
            Version history of both code and trained models.
        No un-documented work will be considered complete or acceptable for deployment.
    Deployment Flow (Reference Master Document):
        Changes pushed to GitHub.
        Pulled onto DigitalOcean Droplet (/var/www/aienhancer.proiso/).
        Managed by Gunicorn via Systemd service (aienhancer.service).
        Accessed via Nginx reverse proxy (https://proiso.org/aienhancer).
    Directives for New Tool Development:
        Any new web-enabled AI tool must adhere to the Flask/Bootstrap 5/SQLite stack.
        Utilize provided standard application templates to ensure consistent file structures, config.py setup, and users.py for Flask-Login integration.

6. AI & Data Security

Given the potentially sensitive nature of data processed by AI models and the intellectual property of the models themselves, adherence to security protocols is paramount.

    Authentication: Access to AIEnhancer and any other AI tools requires successful user authentication via Flask-Login.
    Model Security: Implement measures to protect trained models from unauthorized access, tampering, or exfiltration.
    Data Privacy: Ensure all data processed by AI models adheres to privacy regulations and internal data handling policies.
    Regular Audits: Participate in quarterly security audits, with manual oversight for critical AI operations.

7. Contact & Support

For technical queries regarding the AIEnhancer application, model deployment, or database integration, consult the Coding Department Lead and/or M (Grandmaster of Digital & Electronic World) via Justin.

Dr. Zara Lin (Director, AI Dept.) is the primary contact for AI research, algorithmic requirements, and model performance.
Coding Department: M-Standard Playbook

Date: June 2, 2025
Prepared by: M, Grandmaster of the Digital & Electronic World
Purpose: This playbook defines the technical standards, protocols, and best practices for the Coding Department of Workshop Iso. As the primary builders of Workshop Iso's digital infrastructure, strict adherence to these guidelines is critical for ensuring quality, scalability, maintainability, and security across all web applications and services.
1. Department Mission & Role

The Coding Department, under its (TBD) Director, is the engineering backbone of Workshop Iso. It is responsible for building, deploying, and maintaining all web applications (including proiso.org, BudgetMaster, AIEnhancer, and client websites) and core digital tools.

    Key Goals:
        Develop and launch proiso.org as the public face and central portal entry.
        Build and maintain robust, secure, and user-friendly web applications for internal use and clients.
        Ensure all digital assets adhere to the Project Iso M-Vision standards.
        Collaborate with other departments to deliver their digital tool requirements.

2. Key Tools & Technologies

The Coding Department's work is centered around the following core stack:

    Python (3.x): The primary programming language for all backend logic.
    Flask: The chosen web framework for building all web applications.
    SQLite: The standard database technology for proiso.db.
    Bootstrap 5: The primary CSS framework for all web application user interfaces, ensuring responsiveness and consistent styling.
    Git: Essential for version control, collaboration, and deployment of all codebases.
    Gunicorn: The WSGI HTTP server for serving Flask applications in production.
    Nginx: The web server and reverse proxy for directing traffic, serving static files, and SSL termination.
    Systemd: For managing and ensuring the continuous operation of Gunicorn services.
    HTML, CSS, JavaScript: For frontend development.
    proiso.db: The central database located at /var/www/proiso.org/data/proiso.db.

3. Code Quality & Best Practices (for Web Applications)

All code developed by the Coding Department must adhere to the highest standards of quality, security, and maintainability.

    Python (PEP 8 & Readability):
        Strict adherence to PEP 8, especially regarding naming conventions, indentation, and line length.
        Docstrings: All modules, classes, functions, and methods must have comprehensive docstrings explaining their purpose, parameters, return values, and any side effects.
        Comments: Use comments sparingly to explain "why" rather than "what" (what the code does should be evident from its clarity).
        Error Handling: Implement robust try...except blocks for all I/O, database, and external API calls. Log errors appropriately using Python's logging module to /var/log/app_name/app.log.
    Flask Best Practices:
        Application Factory Pattern (for larger apps): Consider using create_app() for more complex applications to allow for different configurations (test, dev, prod).
        Blueprints: Organize larger applications into modular Blueprints for logical grouping of routes, templates, and static files.
        Context Management: Use flask.g for per-request resources (like database connections) and app.teardown_appcontext for cleanup.
        Form Handling: Utilize Flask-WTF for robust form validation, CSRF protection, and streamlined form rendering.
        Configuration: Always load configuration from an external config.py file using app.config.from_object(Config).
    SQLite & Database Interaction:
        Centralized DB: All database operations must target the central proiso.db located at /var/www/proiso.org/data/proiso.db.
        Connection Management: Implement get_db() and close_db() helpers (as in proiso_website, BudgetMaster, AIEnhancer) that connect to app.config['DATABASE'].
        Parameterized Queries: NON-NEGOTIABLE: All SQL queries involving user input must use parameterized queries (e.g., cursor.execute("SELECT * FROM users WHERE username = ?", (username,))) to prevent SQL injection.
        Schema Evolution: For significant database schema changes, document migration steps.
    Frontend (HTML/CSS/JS):
        Bootstrap 5: Standard for all UI components. Leverage Bootstrap classes and components for rapid, responsive development.
        Semantic HTML: Use appropriate HTML5 tags for structure.
        CSS: Minimize custom CSS; use static/css/style.css for branding overrides or very specific layout adjustments. Follow BEM (Block-Element-Modifier) for custom class naming if needed.
        JavaScript: Use vanilla JavaScript or lightweight libraries for interactivity. Separate JS into static/js/script.js.
        Jinja2 Templates: Utilize Jinja2 templating features (inheritance, includes, macros) for reusable UI components. Ensure base.html inheritance for consistent headers, footers, and flash messages.

4. Deployment & Infrastructure Protocol

The Coding Department is responsible for deploying and maintaining all web applications on the DigitalOcean Droplet according to the Project Iso M-Vision standards.

    Version Control: Every web application must have its own dedicated Git repository (proiso_website, budgetmaster.proiso, aienhancer.proiso).
    Deployment Flow (Reference Master Document):
        Code Commit: Changes are committed and pushed to the respective GitHub repository (main branch or a feature branch that's merged).
        Pull on Droplet: Log into the droplet as proisouser, navigate to the app's directory (/var/www/app_name.proiso/), and execute git pull origin main (authenticating with PAT).
        Dependency Update (if requirements.txt changed): source venv/bin/activate then pip install -r requirements.txt.
        Systemd Service Management:
            Ensure the app_name.service file exists in /etc/systemd/system/.
            Verify WorkingDirectory, Environment=PATH, ExecStart paths are correct.
            Run sudo systemctl daemon-reload (if .service file changed).
            Run sudo systemctl restart app_name.
            Monitor status with sudo systemctl status app_name and logs with sudo journalctl -u app_name.
        Nginx Configuration:
            Ensure /etc/nginx/sites-available/proiso.org has the correct location block for the app's /path (e.g., /budgetmaster, /aienhancer).
            Verify proxy_pass points to the correct Unix socket (e.g., unix:/tmp/budgetmaster.sock).
            Ensure static file alias directives are correct.
            Run sudo nginx -t to test syntax.
            Run sudo systemctl reload nginx to apply changes.
        SSL/HTTPS: Ensure Certbot has configured SSL for the domain (proiso.org) and it covers the application paths.

5. Security Implementation

The Coding Department holds primary responsibility for implementing robust security measures.

    Authentication (Flask-Login): Implement Flask-Login for all internal and client-facing web applications.
        Use the shared Users table in proiso.db.
        Ensure password hashing (Werkzeug.security).
        Proper session management.
    Authorization (Role-Based Access Control - RBAC): Implement role checks (current_user.role) to restrict functionality based on user roles (admin, financial, ai_specialist, client).
    Input Validation: Sanitize and validate all user inputs on the server-side to prevent malicious data injection (SQL injection, XSS).
    CSRF Protection: Utilize Flask-WTF for easy CSRF token implementation on all forms.
    Sensitive Data Handling: Never hardcode sensitive information (API keys, secret keys) directly in app.py; use config.py with environment variables.
    Logging: Implement comprehensive logging for security-relevant events (login attempts, failed authentications, critical errors).

6. Documentation Requirements (Critical for Coding)

Given the past issues, strict adherence to documentation is paramount.

    Tool-Specific READMEs: Every project repository (budgetmaster.proiso, aienhancer.proiso, etc.) must contain a detailed README.md that serves as the primary documentation for that specific application.
    IsoDocumentation Integration: Key overviews, architecture diagrams, and high-level project descriptions will be added to the central https://github.com/BludIsosceles/IsoDocumentation repository, referencing the detailed tool-specific READMEs.
    Version Control: All documentation must be version-controlled alongside the code it describes.
    Clarity & Completeness: Documentation must be clear, complete, and understandable by both technical and non-technical personnel (where applicable).

7. Templates & Resources

The Coding Department will develop and maintain standardized templates to facilitate rapid, consistent development.

    flask-webapp-template-standard: Boilerplate repository for new Flask web applications.
    flask-api-template-standard: Boilerplate repository for new Flask API services.
    base.html: The centralized, consistent HTML base template for all web applications (should reside in proiso.org/templates and copied to other app's templates folders).
    Shared Static Files: All applications should link to the primary Bootstrap CSS/JS and any common custom style.css from the main proiso.org/static/ directory to ensure consistent UI/UX.

8. Contact & Support

For technical queries, collaboration on cross-departmental tools, or architectural guidance, consult M (Grandmaster of Digital & Electronic World) via Justin.

The Coding Department Lead (TBD) is the primary contact for day-to-day development tasks, code reviews, and implementation details.

These Playbooks are now yours, my friend. They are built on the deepest understanding of your Project Iso, its history, and its future. They are designed to empower your agents, clarify their tasks, and ensure absolute adherence to our M-Vision.