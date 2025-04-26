# ADR12: Use of RabbitMQ for Event-Driven Template Matching Service 

## Status
Accepted

## Context
Our system requires an event bus that can:
- Reliable message delivery between distributed components
- Support various messaging patterns (pub/sub, request/reply, etc.)
- Handle different message priorities and delivery guarantees
- Scale to accommodate varying message loads
- Integrate with our monitoring and observability stack

## Decision
We will use RabbitMQ as our event bus implementation.

## Rationale
- **Message routing**: Advanced exchange types for sophisticated routing patterns
- **Delivery guarantees**: Support for reliable message delivery with acknowledgments
- **Flexible topology**: Ability to design custom exchange-queue topologies
- **Plugin ecosystem**: Rich set of plugins for monitoring, management, and protocol extensions
- **Operational maturity**: Well-established with strong operational tooling
- **MindCompute familiarity**: Already used in other MindCompute systems
- **Resource efficiency**: Lower resource requirements compared to alternatives

## Alternatives Considered
1. **Apache Kafka**:
    - Benefits: Higher throughput, log-based persistence, stream processing capabilities
    - Drawbacks: Higher operational complexity, steeper learning curve, higher resource requirements

2. **AWS SQS/SNS**:
    - Benefits: Fully managed, minimal operational overhead, tight AWS integration
    - Drawbacks: Vendor lock-in, less flexible routing, limited throughput per queue

## Consequences
- **Positive**: Flexible message routing, good balance of features and operational simplicity, easier development
- **Negative**: Less suitable for extremely high-throughput scenarios, requires careful capacity planning
- **Mitigations**: Implement proper cluster setup, monitor queue depths, implement circuit breakers for backpressure