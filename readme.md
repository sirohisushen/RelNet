# RelNet 🧠✉️
**Relational Neural Intelligence for Human Communication Analysis & AI-Powered Email Ecosystem**

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.1-red)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## **Overview**
RelNet is a research-driven framework that transforms a user's email history into a **dynamic relational graph** capturing semantic meaning, emotional tone, and relational patterns.  

Beyond analytics, RelNet serves as the foundation for an **AI-powered email ecosystem** capable of drafting context-aware messages that reflect the user's unique communication style.

**Key Features:**
- Semantic, emotional, and temporal embeddings of emails  
- Graph-based modeling of sender-recipient interactions  
- Temporal modeling for communication evolution  
- AI-assisted, context-aware email generation  
- Visualization of relationships, tone, and behavioral patterns  

---

## **Architecture**

### **1. Message Embedding**
Emails are represented along three axes:  
- **Semantic (`s_i`)**: Transformer embeddings  
- **Tone (`t_i`)**: Emotional signature of the message  
- **Context (`c_i`)**: Metadata (timestamps, thread depth, topic)  

v_i = [s_i; t_i; c_i]


### **2. Graph Construction**
- Nodes: Emails, recipients, topics  
- Edges: Reply relationships, semantic similarity, temporal adjacency, tone shift  
- Attributes: Sentiment difference, response latency, topic correlation  

### **3. Graph Neural Network**
R-GCN or GAT propagates embeddings to capture relational patterns and recipient-level style:

h_v^(l+1) = σ( Σ_{r ∈ R} Σ_{u ∈ N_r(v)} W_r h_u^(l) + W_0 h_v^(l) )


### **4. Temporal Dynamics**
Transformers or Temporal Graph Networks model behavior evolution, enabling **context-aware AI email generation**.

---

## **Demo Pipeline**

```mermaid
flowchart LR
    A[Raw Emails] --> B[Preprocessing & Metadata Extraction]
    B --> C[Embeddings: Semantic, Tone, Context]
    C --> D[Graph Construction]
    D --> E[Graph Neural Network]
    E --> F[Temporal Modeling & Style Embeddings]
    F --> G[Analytics & Visualization]
    F --> H[AI Email Generation (Drafts)]
Analytics & Visualization: Tone evolution graphs, relationship heatmaps, clusters of communication archetypes
```
AI Email Generation: Drafts emails respecting tone, style, and context

Quickstart

# Clone the repo
git clone https://github.com/yourusername/RelNet.git
cd RelNet

# Create virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt


Applications
Self-Awareness Tools: Track and analyze your communication style

Corporate Analytics: Detect team communication health and stress patterns

AI-Powered Email Assistants: Context-aware, personalized email drafting

Behavioral Research: Study relational dynamics over time

Autonomous Email Ecosystem: AI-driven drafting and responding while preserving user voice

Evaluation Metrics
Tone & style consistency

Recipient clustering coherence

Predictive accuracy for future tone/style

Quality & contextual relevance of AI-generated emails

Interpretability of insights and visualizations

Tech Stack
Component	Tools / Libraries
Email Processing	Python, Gmail API, FastAPI
Embeddings	OpenAI text-embedding-3-large, HuggingFace Transformers
Graph Modeling	PyTorch Geometric, NetworkX
GNNs	R-GCN, GAT, PyTorch Lightning
Temporal Modeling	Transformers, Temporal Graph Networks
Visualization	Streamlit, Plotly, D3.js
Generation & Summarization	GPT-4, local LLMs

Future Work
Expand beyond email: Slack, chat, and voice transcripts

Integrate causal inference for behavior analysis

Build personalized AI email generation pipelines

Multi-user networks for intelligent, context-aware organizational communication

Feedback loops to refine AI-generated drafts based on user corrections

Ethical Considerations
Raw emails remain local; only embeddings processed

User control over AI-generated emails

Consent-driven data ingestion

Transparent and interpretable models

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
Created by Sushen Sirohi (sushensirohi@gmail.com)