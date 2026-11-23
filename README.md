# Burhan Shabbir Boxwalla
**Senior Software Developer** | [Linkedin](https://uk.linkedin.com/in/burhan-b-074793183)

## Professional Summary
Backend engineer with 5+ years' experience across UK government regulation (Companies House) and Indian life insurance (HDFC Life). My core stack is Java/Spring Boot and Node.js, with Oracle, MongoDB, PostgreSQL, Kafka and AWS.

At Companies House I work across a large, long-lived Oracle/Java platform (CHIPS) and the newer cloud microservice estate. I deliver legislative and regulatory change end to end: discovery spikes, design, multi-repository implementation, database patches, test automation, pipelines and environment configuration. At HDFC Life I progressed from graduate trainee to senior engineer in two years, leading the backend of a customer-facing payout journey and building shared platform services. I have mentored engineers, presented to non-technical stakeholders, and I am looking to step into a technical lead role.

## Technical Skills

| Area | Details |
|---|---|
| Languages | Java 8–21, JavaScript, TypeScript, SQL and PL/SQL, Python, Groovy, HTML/CSS |
| Frameworks | Spring Boot 2/3/4, Hibernate, Node.js, Express (Helmet, CSRF middleware), REST APIs, microservice architecture |
| Data and messaging | Oracle, MongoDB, PostgreSQL, Apache Kafka (consumers, retry/error topics, delta consumers) |
| Cloud and infrastructure | AWS (ECS, S3, Parameter Store), Terraform, Docker/docker-compose, Ansible, OpenTelemetry |
| CI/CD and quality | Concourse, Jenkins, SonarQube, OWASP dependency-check, Maven, npm |
| Testing | JUnit, Mocha, Karate API tests, integration and regression testing, Postman, Bruno |
| Integrations | GOV.UK Notify, OpenAPI/REST specifications, LDAP, HMCTS CPPI, payment gateways, SMS/WhatsApp |
| Ways of working | Agile, time-boxed spikes, code review, mentoring, stakeholder presentations, Git/GitHub/Bitbucket, Jira, Confluence |
| Spoken languages | English, Hindi, Urdu |

## Professional Experience

### Companies House, UK
**Senior Software Developer** *(Oct 2024 – Present)* | **Software Developer** *(Sept 2023 – Sept 2024)*

*Java, Spring Boot, Node.js, Oracle SQL, MongoDB, Kafka, Docker, AWS, Terraform*

Companies House maintains the public register of UK companies and enforces filing and compliance obligations. My work spans the internal case-management system (CHIPS), its supporting REST and Kafka services, and public-facing web services.

**Strike-off compliance and Expedited Strike Off**
- Developed the default-address strike-off compliance path, including a new gazette image, new database parameters and thorough testing. It resulted in the removal of about 9,000 fraudulent companies from the register.
- Delivered the Expedited Strike Off (ESO) lifecycle in CHIPS: start and end of ESO, validation, "sight required" handling, default investigation stops, a voluntary-dissolution reinstatement privilege, and post-GAZ2 edge cases.
- Implemented the Default Return of Accounts/Annual Return strike-off path and its moves to the compulsory strike-off paths (DEFSTATAC/AR/B), including signs of activity, accounts-received handling, force-compliance checks and GAZ1 images for companies and LLPs.
- Ran regression testing of the overnight compliance triggers and many time-boxed spikes (ESO intercept, DS01→ES01→ES02 flow, grace filing period, RP09/RP10), each producing a recommendation the team could plan from.
- Propagated ESO corporate annotations through the delta pipeline: `chs-delta-api`, `company-profile-delta-consumer`, private API SDK and specifications, `api-enumerations` and the public site. This was a coordinated change across seven repositories.

**Identity Verification (IDV) compliance and enforcement**

*Context: mandatory IDV launched on 18 November 2025 for all directors and PSCs, with a year-long transitional period.*
- Delivered the compliance and enforcement workflows for the IDV project, which has resulted in over 500,000 companies being removed from the register through dissolution and over 1,300 financial penalties for late confirmation statements and IDV statements.
- The same enforcement pathway has led to the prosecution of 195 companies and 204 directors, 131 convictions, and the first director disqualifications. It has also supported over 70,000 representations and around 1,300 referrals to the Insolvency Service.
- Delivered new org units and contact classifications for the IDV Compliance and Enforcement service across England & Wales, Scotland and Northern Ireland.
- Built the CS01-driven IDV compliance case type, plus PSC pursuit types, configurable pursuit parameters, close reasons, and event-driven handling for ES01, VS01 and PSC07 with automatic closure and work-item creation.
- Delivered letters and emails (CSIDVREM, CSIDVDEFLET, IDVPSCDEFAULT, director chaser, DEF50) through GOV.UK Notify and the Document Exchange Engine. This covered template versioning, Welsh-language templates and dates, and economy-postage selection.
- Added a feature flag for safe release of a date-sensitive letter change, and moved Notify message persistence into the sender API to simplify data ownership.

**New services and platform engineering**
- Bootstrapped two new Java 21 microservices (`cis-cppi-api`, `cis-prosecution-api`) from skeleton to deployable. This included Dockerfiles, healthchecks, Terraform, CI pipelines, shared-infrastructure config, SonarQube onboarding and local-dev modules.
- Led the discovery on integrating with the HMCTS CPPI service, including its Open API specification.
- Upgraded `cis-api` and `kafka-error-consumer` to Spring Boot 4, and wrote an integration suite covering every Kafka consumer scenario. Added a retry-topic bootstrap, Kafka 3 and OpenTelemetry to the shared development environment.
- Improved pipeline reliability by making release builds depend on passing integration tests, and moved CHIPS builds to the new Concourse E2E pipeline.

**ECMS case-management integration**
- Created new contact-case and contact–appointment link tables with CHIPS REST admin endpoints.
- Delivered an `OWNED_BY_ECMS` ownership flag across the database, Hibernate model and CIS API, and a feature-flagged ECMS notification endpoint for LFP appeals post-room contact.
- Set up ECMS service access including LDAP, and fixed a CIS API defect in officer-name mapping for corporate-body appointments.

**Security, quality and shared services**
- Hardened the public Strike Off Objections service: Content Security Policy via Helmet (no `unsafe-inline`), re-enabled CSRF protection with a fix for empty tokens, secure cookie flags, a middleware-bypassing healthcheck, and a document-download redirect vulnerability.
- Fixed critical, high and moderate vulnerabilities across 10+ Java and Node services and shared libraries, reducing technical debt by an estimated 10%.
- Enhanced the restricted words service and rule engine with 4 new categories and specific rejection messages, with API, web and Karate test changes.
- Migrated the Strike Off Objections API to the new file-transfer-service, fixing attachment-download failures, and integrated the Oracle query API.

**Leadership and communication**
- Mentored a new team member to handle tickets independently within 1 month.
- Presented project results to stakeholders, improving understanding between technical and non-technical teams.

### HDFC Life, India — Senior Software Engineer *(July 2022 – Aug 2023)*
*Node.js, Express, MongoDB, PostgreSQL, Docker, AWS*
- Led backend development of the maturity payout journey, designing and building REST APIs and reducing processing time from 2 working days to 15 minutes.
- Integrated a payment gateway and built analytics reports for rider renewal, resulting in a 20% increase in revenue from rider sales.
- Created a vendor-agnostic microservice for SMS and WhatsApp notifications, adopted by internal teams as the shared notification platform.
- Coordinated with intra- and inter-team members to resolve dependencies, ensuring 90% on-time project delivery.

### HDFC Life, India — Graduate Trainee *(July 2021 – July 2022)*
*Node.js, Express, MongoDB, PostgreSQL, Docker, AWS*
- Built an email portal for call-centre teams, improving their productivity by 30%.
- Delivered bug fixes and new features in Node.js and Express.
- Mastered the company's tech stack in 6 months, enabling effective collaboration with senior developers and faster development.

### SAP Labs, Bengaluru — Intern *(Aug 2020 – Dec 2020)*
*Node.js, Groovy, Jenkins, AWS*
- Developed proof-of-concept solutions for cloud platform backing services. The prototype led to a new database offering and improved data storage efficiency.
- Assisted the DevOps team with Jenkins pipeline automation, improving deployment efficiency.

### Indian Meteorological Department — Intern *(May 2019 – July 2019)*
*HTML, PHP, MySQL*
- Created an observatory management portal that streamlined instrument status tracking.

## Education
**Bachelor of Engineering in Computer Science**, Birla Institute of Technology & Science, Pilani *(Aug 2017 – July 2021)*

**Minor in Finance**, Birla Institute of Technology & Science, Pilani
