### ADR 3: Event-Driven Architecture for Process Automation

**Context**:
Many interview scheduling workflows require coordination across multiple systems and stakeholders, with manual handoffs creating delays and inconsistencies.

**Decision**:
Implement an event-driven architecture to automate workflows and notifications across the interview scheduling process.

**Rationale**:
- Enables real-time reactions to changes in availability, scheduling, and feedback
- Reduces manual coordination between systems and stakeholders
- Allows for flexible process definitions that can evolve without code changes
- Supports asynchronous processing for better scalability

**Consequences**:
- Introduces complexity in event management and error handling
- Requires clear event schemas and versioning strategy
- Creates potential for race conditions if not carefully designed
- May require additional monitoring for event flow visibility