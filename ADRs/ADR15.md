# ADR 15: TensorFlow for NLP Component

## Status
Accepted

## Context
Our system requires NLP capabilities to:
- Extract entities and intent from interview requests
- Analyze technical skills and requirements
- Match candidates to appropriate interview templates
- Process interview feedback for insights

We need to select an ML framework that supports these requirements while fitting into our development and deployment workflows.

## Decision
We will use TensorFlow/Keras as our primary ML framework for NLP components.

## Rationale
- **Production readiness**: Strong support for model serving in production
- **Comprehensive ecosystem**: Libraries for NLP, text processing, and model deployment
- **Model optimization**: Tools for model optimization and mobile deployment
- **Scalability**: Support for distributed training and inference
- **Deployment options**: TensorFlow Serving, TF Lite, and TensorFlow.js compatibility
- **Community support**: Large community and extensive documentation
- **Integration capabilities**: Good integration with Python ecosystem
- **Model versioning**: Built-in support for model versioning and A/B testing

## Alternatives Considered
1. **PyTorch**:
   - Benefits: More intuitive API, better for research, dynamic computation graph
   - Drawbacks: Less mature production deployment tools, more complex serving infrastructure

## Consequences
- **Positive**: Robust framework for both development and production, good alignment with our technical requirements
- **Negative**: Steeper learning curve, higher resource consumption than simpler frameworks
- **Mitigations**: Use pre-trained models where possible, standardize on TF 2.x API, implement model optimization
