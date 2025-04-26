### ADR 11: Single-Region Containerized Deployment

**Context**:
The system needs to be deployed for MindCompute India operations, with all interviews and documentation managed within a single region.

**Decision**:
Deploy PIPO as containerized microservices in a single Kubernetes cluster in India with appropriate redundancy and scaling capabilities.

**Rationale**:
- All interviewing operations are centralized in India
- Data residency requirements are simplified with single-region deployment
- Resource optimization can be achieved within a single cluster
- Operations and maintenance are simplified

**Consequences**:
- Simplified deployment and operations
- Reduced infrastructure and operational costs
- Improved latency for India-based users
- Future expansion to other regions would require architecture modifications