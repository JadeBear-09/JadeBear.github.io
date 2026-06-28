# Jyotishna

Data Scientist and IIT Delhi graduate building production-style AI systems.

I focus on practical AI engineering: retrieval systems, model-serving workflows,
monitoring, guardrails, and deployed demos that can be inspected directly.

## Featured Projects

### TelcoAssist RAG

Production-style telecom RAG platform for support, policy, and network operations.
It combines hybrid retrieval, reranking, source citations, confidence scoring,
fallback behavior, guardrails, ACL-before-retrieval, audit logs, and deployment
health checks.

- Live demo: [TelcoAssist Query UI](http://telcoassist-demo-alb-1864469644.us-east-1.elb.amazonaws.com/query)
- Health check: [TelcoAssist Health](http://telcoassist-demo-alb-1864469644.us-east-1.elb.amazonaws.com/health)
- Ready check: [TelcoAssist Ready](http://telcoassist-demo-alb-1864469644.us-east-1.elb.amazonaws.com/ready)
- GitHub: [JadeBear-09/telcoassist-rag](https://github.com/JadeBear-09/telcoassist-rag)
- Stack: FastAPI, Qdrant, BM25, hybrid retrieval, reranking, Docker, AWS ALB

### D-Lens

Diagnostic API for failed chatbot, RAG, and agent responses. It accepts traces,
detects failure signals, assigns severity, returns structured root-cause reports,
stores reports, supports similar-failure search, and exposes monitoring endpoints.

- Live API docs: [D-Lens Swagger](https://dlens-api-wuscfbl3cq-el.a.run.app/docs)
- Health check: [D-Lens Health](https://dlens-api-wuscfbl3cq-el.a.run.app/health)
- GitHub: [JadeBear-09/faillens_ai_docs](https://github.com/JadeBear-09/faillens_ai_docs)
- Stack: FastAPI, Pydantic, Postgres, Cloud Run, Cloud SQL, Prometheus metrics

### Telecom Churn Risk Engine

End-to-end classical ML project for telecom churn prediction and retention
recommendations. It includes model training, threshold tuning with business costs,
explainability, FastAPI serving, Streamlit dashboarding, Docker deployment, tests,
and monitoring snapshots.

- Live demo: [Hugging Face Space](https://huggingface.co/spaces/Jade09/telecom-churn-risk-engine)
- Direct app: [Telecom Churn App](https://jade09-telecom-churn-risk-engine.hf.space)
- GitHub: [JadeBear-09/traditional-ML-project](https://github.com/JadeBear-09/traditional-ML-project)
- Stack: Python, scikit-learn, FastAPI, Streamlit, Docker, pytest, Hugging Face Spaces

## What I Build

- Retrieval-augmented generation systems with citations and fallback behavior
- AI monitoring and diagnostic tools for production-style failure analysis
- ML decision systems that connect predictions to business actions
- Deployed demos with health checks, documentation, and resume-ready links
