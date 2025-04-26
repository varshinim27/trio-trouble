### ADR 4: Automated Tag Management System

**Context**:
Interviewer skills and preferences are currently managed manually, leading to outdated information and inappropriate interviewer selection.

**Decision**:
Implement an automated tag management system that updates interviewer skills and preferences based on multiple data sources.

**Rationale**:
- Ensures interviewer tags remain accurate and current
- Reduces manual maintenance burden on TalOps team
- Addresses a primary cause of interview cancellations
- Creates foundation for better matching and scheduling

**Consequences**:
- Requires access to multiple data sources (MyMindComputeProfile, project assignments, etc.)
- Needs clear rules for tag updates, expirations, and validations
- Must balance automation with appropriate human verification
- Will need mechanisms for interviewers to review and correct automated updates