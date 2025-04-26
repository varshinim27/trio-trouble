### ADR 9: Event-Driven Architecture for PIPO

**Context**:
PIPO requires integrating multiple systems (e.g., VideoMeetingConnector, Salesforce, InterviewLogger) to handle multiple events asynchronously 

**Decision**:
Implement an event-driven architecture with a central event bus and dedicated processors that can manage their independent processing while ensuring the system remains resilient, scalable, and responsive under varying load conditions.

**Rationale**:
- Events like `meeting.ended` or `recording.completed` from VideoMeetingConnector can arrive at different times. EDA allows for independent processing of each event and subsequent correlation without waiting for all information to be available.
- External systems have varying response times and availability
- If downstream systems (Salesforce, InterviewLogger) are temporarily unavailable, events can be stored and processed later ensuring the resilience to system failures
- Each integration has independent retry policies and circuit breakers so failure in one subsystem doesn't affect the entire workflow

- Events related to the same interview can be easily correlated using meeting IDs

**Consequences**:
- Improved resilience and fault tolerance
- Better scalability during peak interview periods
- Additional complexity in implementation
