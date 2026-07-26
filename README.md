<div align="center">

# Hi, I'm Abdramane Mahamat Adji Zezerti 👋

### Information Systems Graduate · Building Enterprise Software That Runs Real Operations

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdramane-m-a0a047316/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:amazezerti0103@gmail.com)
[![Open to Relocate](https://img.shields.io/badge/Open%20to-Relocation%20%26%20Visa%20Sponsorship-2ea44f?style=for-the-badge)](https://www.linkedin.com/in/abdramane-m-a0a047316/)

</div>

---

## About Me

I'm an Information Management graduate who builds enterprise software that helps organizations run their day-to-day operations: inventory, warehouses, finance, and business workflows — more effectively.

I enjoy transforming business requirements into scalable software solutions, with a strong focus on system architecture, database design, automation, inventory management, digital transformation, and enterprise workflows. My goal is to build technology that improves how organizations manage information, resources, and decision-making.

Currently seeking international opportunities as a **Junior Software Developer**, **Information Systems Analyst**, **Business Systems Analyst**, or **IT Systems Officer**.

---

## What Makes Me Different

I enjoy building software for real organizations. My projects span retail (a multi-branch inventory ERP), healthcare (a hospital lab management system), national government (an exam board's candidate-to-certificate pipeline), and commerce (an e-commerce platform) — each one solving an actual operational problem for an organization that runs on it, not a toy exercise.

I design business workflows before I write code, because understanding how an organization actually operates is just as important as implementing the software for it.

---

## Technical Skills

<img src="https://skillicons.dev/icons?i=python,django,flask,java,spring,hibernate,maven,dart,flutter,firebase,ts,nodejs,express,postgres,sqlite,supabase,js,html,css,react,bootstrap,git,github,githubactions,docker,linux,windows,vscode,nginx,redis,prometheus,grafana,vercel&perline=12" />

| Category | Skills |
|---|---|
| **Languages** | Python · SQL · Java · TypeScript · JavaScript · Dart · HTML · CSS |
| **Backend** | Django · Django REST Framework · Flask · Spring Boot · Spring Security · Hibernate / Spring Data JPA · Node.js · Express · Celery (background/scheduled tasks) |
| **Frontend & Mobile** | React (incl. TypeScript) · Vite · TailwindCSS · Thymeleaf · Bootstrap · Flutter |
| **Database & Storage** | PostgreSQL (incl. triggers) · SQLite · Supabase · MinIO / S3-compatible storage · Cloudinary |
| **Infrastructure & DevOps** | Docker · Docker Compose · Nginx · Redis · GitHub Actions (CI/CD) · Prometheus · Grafana · Vercel · Render · Firebase · Flyway · Maven · Git · GitHub · VS Code · Linux · Windows |
| **Concepts** | Object-Oriented Programming · Database Design & Migrations · REST API Design · Authentication & Authorization · Role-Based Access Control (RBAC) · Two-Factor Authentication (TOTP) · Encryption at Rest · Automated Testing · CI/CD Pipelines · Observability & Monitoring · System Analysis & Design · Information Systems · Inventory & Warehouse Management · Business Process Automation |

---

## Featured Projects

### 🏬 Smart Stock & Warehouse Control System (SSWCS) — AKM SARL

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=amazezerti&repo=akm_sarl_sswcs&theme=default)](https://github.com/amazezerti/akm_sarl_sswcs)

A full-stack enterprise ERP built for a real multi-branch retail/wholesale business, covering the full operational loop: multi-branch and multi-warehouse inventory (down to zone/rack/bin level), a POS-style sales workflow, procurement (purchase orders, goods-received notes, supplier returns), logistics/stock transfers, and accounting (expenses, profit & loss, KPI targets).

- Designed a **role-based access model** (HQ Admin, Branch Manager, Warehouse Manager, Accountant) with data scoping enforced server-side, not just hidden in the UI
- Built a **customer credit management workflow** — customers captured automatically from sales, configurable credit limits, and a branch-scoped approval/settlement process
- Implemented **secure, cookie-based authentication** with session invalidation on password change, OTP-based password reset, and an **immutable audit log** of account activity and stock movements
- Automated business alerts (low stock, expiry dates, delayed transfers, expense thresholds) via scheduled background tasks, with branded PDF/Excel/CSV report exports
- **Stack:** Django REST Framework · React · PostgreSQL · Redis · Celery · Docker · Nginx

---

### 🎓 ONECS — National Baccalauréat Exam Management System (Chad)

[ONECS — Office National des Examens et Concours du Supérieur](https://github.com/amazezerti/onecs_oems) *(repository currently private)*

A large-scale information system digitizing the Republic of Chad's national baccalauréat (BAC) exam administration end to end — candidate registration, region-scoped centre and seat assignment, double-blind grading, jury deliberation, results publication, and tamper-evident certificate issuance with public QR-code verification.

- Modeled **six distinct roles** across the real exam-board hierarchy (Super Admin, National Admin, Academy Delegate, Grading Coordinator, School, Candidate), each scoped to their own academy, centre, or subject at both the API and database layer
- Built a **double-blind grading and deliberation pipeline** — automatic grade-stub creation when a session enters grading, statistical outlier detection, and a jury decision workflow that can trigger automatic re-certification through the appeals process
- Engineered **certificate integrity** with HMAC-SHA256 signing and constant-time verification at a public, rate-limited endpoint that returns zero personal data — only pass/mention/serial metadata
- Enforced a **hard, no-bypass registration deadline** and an **immutable audit log** (a PostgreSQL trigger rejects any UPDATE/DELETE on it), on top of mandatory TOTP 2FA for every high-privilege role and Fernet-encrypted candidate data at rest
- Shipped a full observability and deployment stack — Prometheus + Grafana, Celery/Redis for bulk uploads and scheduled encrypted backups, MinIO object storage, Nginx, and a GitHub Actions CI pipeline (flake8, black, bandit, pip-audit, pytest)
- **189 automated tests, 0 failures**, covering both the Django backend and the React/TypeScript frontend
- **Stack:** React (TypeScript) · Django REST Framework · PostgreSQL · Celery + Redis · MinIO · Docker Compose

---

### 🏥 Al-Shifa Medical Laboratory Management System (MLMS)

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=amazezerti&repo=mlms_Al_Shifa&theme=default)](https://github.com/amazezerti/mlms_Al_Shifa)

A role-based clinical laboratory management system built for Al-Shifa Hospital in N'Djamena, Chad, digitizing the full lab workflow from patient registration to billing.

- Modeled the complete clinical pipeline end to end: a **Receptionist** registers the patient → they're assigned to a **Doctor** (load-balanced by department) → a lab test order is created and confirmed → a **Lab Technician** collects the sample and enters results → the **Doctor** verifies them → the **Receptionist** prints the report and processes payment
- Implemented **four distinct roles** (Admin, Receptionist, Doctor, Lab Technician), each with its own Spring Security-enforced permissions
- Used Flyway for versioned database migrations and Hibernate / Spring Data JPA for the persistence layer
- **Stack:** Java, Spring Boot, Spring Security, PostgreSQL, Hibernate, Flyway, Thymeleaf, Bootstrap, Maven

---

### 🛒 Société Ma-Moussa SARL — E-Commerce Platform

[Société Ma-Moussa SARL — E-Commerce Website](https://github.com/amazezerti/ma-moussa_SARL) *(repository currently private)* · live at [ma-moussa-sarl.vercel.app](https://ma-moussa-sarl.vercel.app)

A full-stack e-commerce website built and deployed for Société Ma-Moussa SARL, a real business in N'Djamena, Chad.

- Built a **hardened admin panel** behind a secret, rate-limited, code-split URL — absent from navigation, source comments, and `robots.txt`, so it never appears in the public JS bundle
- Implemented **defense-in-depth security**: httpOnly + Secure + SameSite=Strict JWT cookies, bcrypt (12 rounds), Helmet.js headers, strict CORS, tiered rate limiting (a global cap plus a much tighter one on login), input sanitization, and parameterized SQL throughout
- Uploaded images stream directly to Cloudinary with server-side MIME and size validation — they never touch the server's disk
- Designed for a clean, environment-driven deploy: PostgreSQL locally, a one-line switch to Supabase in production, zero code changes required
- **Stack:** React + Vite + TailwindCSS · Node.js + Express · PostgreSQL / Supabase · Cloudinary · Vercel + Render

---

### 📱 Class Assignments — Mobile (Flutter)

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=amazezerti&repo=ClassAssignments-Mobile-&theme=default)](https://github.com/amazezerti/ClassAssignments-Mobile-)

A cross-platform mobile app built to practice full-stack mobile development beyond the web — product inventory with local storage, cloud authentication, and device-level integrations.

- Product CRUD with a local SQLite database and image storage
- Firebase Authentication with Google Sign-In, plus push notifications via Firebase Cloud Messaging
- Device-level integrations: Bluetooth scanning, battery-level monitoring, connectivity status, and contacts access with permission handling
- Light/dark theme toggle
- **Stack:** Flutter, Dart, Firebase (Auth, Messaging, Core), SQLite

---

## Currently Learning

🌱 Enterprise Software Architecture
🌱 Cloud Deployment
🌱 REST API Design at Scale
🌱 PostgreSQL Performance & Optimization
🌱 Scalable Backend Development

---

## Next Milestones

- [ ] AWS Cloud Practitioner
- [ ] Microsoft AZ-900 (Azure Fundamentals)
- [ ] GitHub Foundations

---

## Languages

🇬🇧 English &nbsp;&nbsp; 🇫🇷 French &nbsp;&nbsp; 🇸🇦 Arabic

---

## Open to Opportunities In

🇨🇦 Canada &nbsp;&nbsp; 🇩🇪 Germany &nbsp;&nbsp; 🇳🇱 Netherlands &nbsp;&nbsp; 🇮🇪 Ireland &nbsp;&nbsp; 🇱🇺 Luxembourg

Open to relocation and visa sponsorship.

---

## A Few Things About How I Work

⚡ I design business workflows before writing code
⚡ I believe understanding a business process is just as important as writing the software for it
⚡ I enjoy turning complex organizational requirements into practical information systems

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=amazezerti&show_icons=true&theme=default&count_private=true" height="165" alt="GitHub stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=amazezerti&theme=default" height="165" alt="GitHub streak stats" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=amazezerti&theme=minimal" alt="GitHub activity graph" />
</p>

---

## Contact

📧 **Email:** [amazezerti0103@gmail.com](mailto:amazezerti0103@gmail.com)
💼 **LinkedIn:** [linkedin.com/in/abdramane-m-a0a047316](https://www.linkedin.com/in/abdramane-m-a0a047316/)
🌐 **Portfolio:** coming soon

