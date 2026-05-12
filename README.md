# CancerCare-AI
CancerCare AI — Multi-Agent Cancer Risk &amp; Nutrition Intelligence Platform

## Main Objective

### Build a multi-agent AI system that:

    Predicts cancer probability using ML models
    Analyzes patient symptoms/reports
    Uses RAG + web search for cancer guidance
    Suggests nutrition/lifestyle recommendations
    Provides stage-aware assistance
    Maintains conversational memory
    Tracks all experiments/evaluations
    Uses production-grade LLMOps + AI Engineering stack


                   ┌─────────────────────┐
                   │    User / Doctor    │
                   └──────────┬──────────┘
                              │
                    FastAPI / Streamlit UI
                              │
               ┌──────────────┴──────────────┐
               │      LangGraph Orchestrator │
               └──────────────┬──────────────┘
                              │
      ┌────────────────────────────────────────────┐
      │                Multi Agents                │
      └────────────────────────────────────────────┘


       ┌──────────────┐
       │ Intake Agent │
       │ symptom/data │
       └──────┬───────┘
              │
       ┌──────▼────────┐
       │ Prediction    │
       │ Agent         │
       │ sklearn/xgb   │
       └──────┬────────┘
              │
       ┌──────▼────────┐
       │ RAG Agent     │
       │ cancer docs   │
       └──────┬────────┘
              │
       ┌──────▼────────┐
       │ Web Research  │
       │ Agent         │
       │ nutrition     │
       └──────┬────────┘
              │
       ┌──────▼────────┐
       │ Nutrition     │
       │ Recommendation│
       │ Agent         │
       └──────┬────────┘
              │
       ┌──────▼────────┐
       │ Safety Agent  │
       │ hallucination │
       │ verification  │
       └──────┬────────┘
              │
       ┌──────▼────────┐
       │ Response      │
       │ Agent         │
       └───────────────┘
    
    
──────────────────────────────────────────
    
### Backend Systems
    
    1. ETL + Medallion Architecture
       Bronze -> Silver -> Gold
    
    2. Vector DB
       Chroma / Weaviate / PGVector
    
    3. MLflow
       experiment tracking
       prompt tracking
       agent evaluation
    
    4. Observability
       LangSmith
       DeepEval
       RAGAS

    5. Optimization
       reranker
       context compression
       token minimization
    
    6. Deployment
       Docker
       Kubernetes
       CI/CD
