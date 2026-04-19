# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

> **Naming conventions used throughout these docs:**
> - **PM** = Project Manager
> - **PdM** = Product Manager

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers (PdM) define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers (PM) coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Release Manager

### Role Summary
The Release Manager coordinates all release activities, ensuring the team meets pre-release requirements, manages deployment schedules, and communicates rollout and rollback strategies. See [Release & Deployment](octoacme-release-and-deployment.md) for the full release process.

### Responsibilities
- Own and maintain the release schedule and deployment plan
- Confirm all pre-release criteria are met (acceptance criteria, CI, security scans, release notes)
- Coordinate go/no-go decisions with the PM, QA Lead, and DevOps Engineer
- Document and communicate rollback plans and incident playbooks
- Announce releases to stakeholders and the support team

### Goals
- Achieve predictable, low-risk releases
- Minimize production incidents caused by deployments
- Maintain clear audit trails for every release

### Typical Communication
- Pre-release go/no-go meeting with PM, QA Lead, and DevOps Engineer
- Release announcements to stakeholders and support channels
- Post-deploy status updates and incident reports (if needed)

### Interactions with Existing Roles
- **PM**: Aligns release dates with project milestones and communicates schedule changes.
- **PdM**: Confirms which features are in scope for each release; obtains sign-off on release notes.
- **Developers**: Reviews merged PR list and confirms all required PRs are included before deploying.

---

## UX Designer

### Role Summary
UX Designers advocate for user needs across the delivery lifecycle. They produce design specifications, validate usability, and collaborate with Developers and PdMs to ensure the product is intuitive and accessible.

### Responsibilities
- Conduct user research and synthesize findings into actionable insights
- Create wireframes, prototypes, and design specifications
- Participate in iteration planning and sprint reviews to provide design feedback
- Validate implemented features against design intent and usability standards
- Champion accessibility and inclusive design practices

### Goals
- Ensure the product is usable, accessible, and delightful for end users
- Reduce rework by providing clear, well-reviewed design assets early
- Bridge the gap between user needs and technical implementation

### Typical Communication
- Design reviews and walkthroughs with Developers and PdM
- Usability testing sessions and synthesis reports
- Design handoff notes (e.g., annotated Figma files or design specs in the project repo)

### Interactions with Existing Roles
- **PM**: Raises design-related risks or timeline concerns during planning; provides effort estimates for design tasks.
- **PdM**: Co-defines acceptance criteria for usability; aligns design direction with product vision and user research.
- **Developers**: Delivers design specs and responds to implementation questions; reviews completed UI against designs during QA.

---

## DevOps Engineer

### Role Summary
DevOps Engineers maintain the CI/CD pipelines, infrastructure reliability, and deployment tooling that enable the team to ship safely and continuously. See [Execution & Tracking](octoacme-execution-and-tracking.md) for pipeline and workflow expectations.

### Responsibilities
- Build, maintain, and improve CI/CD pipelines and deployment automation
- Monitor system health, uptime, and performance
- Manage environment configuration, secrets, and access controls
- Support incident response and root-cause analysis for infrastructure issues
- Collaborate on security scanning and vulnerability remediation

### Goals
- Enable fast, reliable, and repeatable deployments
- Reduce toil through automation and self-service tooling
- Maintain high availability and observability across environments

### Typical Communication
- Pipeline status alerts and deployment notifications
- Infrastructure change proposals and post-incident reports
- On-call escalation during incidents

### Interactions with Existing Roles
- **PM**: Communicates infrastructure constraints or planned maintenance windows that may affect the project schedule.
- **PdM**: Advises on scalability and reliability implications of proposed features.
- **Developers**: Partners on pipeline configuration, environment parity, and debugging deployment issues.

---

## QA Lead

### Role Summary
The QA Lead oversees test planning, coordinates manual and automated testing, and enforces quality gates throughout the delivery cycle. See [Execution & Tracking](octoacme-execution-and-tracking.md) for the quality and testing workflow.

### Responsibilities
- Define and maintain the test strategy, including unit, integration, and end-to-end test coverage
- Coordinate manual QA for feature acceptance when needed
- Own the definition of quality gates and the "Definition of Done"
- Track and triage defects; prioritize with PM and PdM
- Approve releases from a quality perspective as part of the go/no-go process

### Goals
- Prevent defects from reaching production
- Ensure the "Definition of Done" is consistently applied
- Reduce manual testing overhead through automation

### Typical Communication
- QA status updates in weekly delivery syncs
- Defect reports and triage notes on project board
- Go/no-go sign-off for each release

### Interactions with Existing Roles
- **PM**: Reports on test status, open defects, and any quality risks that may affect the release schedule.
- **PdM**: Clarifies acceptance criteria and assists in defining measurable quality expectations.
- **Developers**: Reviews and provides feedback on test coverage; pairs on debugging complex defects.

---

## Subject Matter Expert (SME)

### Role Summary
Subject Matter Experts provide deep domain knowledge—technical, regulatory, or business—that the core team may lack. They act as advisors and reviewers to reduce risk and improve correctness. See [Risk Management & Communication](octoacme-risks-and-communication.md) for how SME input feeds into risk assessment.

### Responsibilities
- Review artifacts (specs, designs, release notes) for domain accuracy and compliance
- Advise on risks, dependencies, and edge cases specific to their domain
- Participate in planning sessions when domain complexity is high
- Act as an escalation point for domain-specific questions during execution

### Goals
- Reduce defects and rework caused by domain misunderstandings
- Ensure the team's solutions are compliant with regulatory or business constraints
- Accelerate decision-making by providing timely, authoritative input

### Typical Communication
- Async review of documents and PRs with annotated feedback
- Scheduled advisory sessions during planning or at key milestones
- On-call consultation for urgent domain questions during execution

### Interactions with Existing Roles
- **PM**: Aligns on which artifacts require SME review and when; flags domain-driven risks to the risk register.
- **PdM**: Validates problem statements and success metrics against domain realities.
- **Developers**: Reviews technical designs and implementation plans to identify domain-specific issues early.

---

## Responsibilities & Hand-offs (RACI Summary)

The table below summarises primary responsibilities across key project activities. Use it to clarify ownership and reduce ambiguity at hand-off points.

| Activity | PM | PdM | Developer | Release Manager | UX Designer | DevOps Engineer | QA Lead | SME |
|---|---|---|---|---|---|---|---|---|
| Project planning & scheduling | **R/A** | C | C | I | I | I | I | C |
| Backlog prioritisation | C | **R/A** | C | I | C | I | I | C |
| Feature design & specs | I | A | C | I | **R** | I | C | C |
| Implementation & code review | I | I | **R/A** | I | C | C | C | I |
| CI/CD pipeline & environments | I | I | C | C | I | **R/A** | I | I |
| Test strategy & quality gates | C | C | C | I | I | C | **R/A** | C |
| Release planning & go/no-go | A | C | I | **R** | I | C | C | I |
| Risk identification & tracking | **R/A** | C | C | C | I | C | C | C |
| Stakeholder communication | **R/A** | C | I | C | I | I | I | I |
| Domain accuracy review | I | C | I | I | I | I | I | **R/A** |

**Key:** R = Responsible · A = Accountable · C = Consulted · I = Informed

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

