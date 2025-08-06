## VAASTHU VISION AI — REPORT.md

### 1. TEAM INFORMATION:
- **Team Name**: VaasthuVision  
- **Members & Roles**:
  - **Shiva Prasad Naroju** – Team Lead, AI/ML Engineer.
  - **Vaishnavi** – UX/UI Designer, Data Engineer & Prompt Engineer.
  - **Akshaya** – Performance Analyst, Feedback coordinator & Documentation Support.
- **Contact**: xxxxxxxx

---

### 2. APPLICATION OVERVIEW:
- **App Name**: Vaasthu Vision AI  
- **Problem It Solves**:  
  Home design often gets delayed because people have to consult both architects and Vaasthu experts separately.
- **MVP Built**:  
  A responsive AI chatbot website that gives instant Vaasthu guidance using a RAG-based pipeline.  

---

### 3. AI INTEGRATION DETAILS:
- **Open-source Models Used**:
  - `llama3-8b-8192` via Groq
  - `all-MiniLM-L6-v2` (SentenceTransformers)
- **Tasks Performed**:
  - Vaasthu Q&A via semantic search
  - Handles fallback queries
- **Data Collection Support**:
  - Generates tagged, intent-classified Vaasthu conversations
  - Enables automatic corpus growth

---

### 4. TECHNICAL ARCHITECTURE:
- **Frontend**:  
  - Built fully responsive and interactive website. 
- **Backend Logic**:  
  - FastAPI  
  - `critical_keywords()` for routing  
  - Fallback system for non-Vaasthu queries
- **AI/ML Integration**:  
  - Qdrant vector search with chunked `.txt` rules  
  - Deterministic prompting for short answers
- **Storage**:  
  - Plaintext rule files converted to vector embeddings  
- **Offline-first**: Planned via local inference

---

### 5. USER TESTING & FEEDBACK (Week 2):
- **Testers**: Through meetups, hackathons, WhatsApp  
- **Tasks**:
  - Vaasthu queries: "Can pooja room be above bathroom?"  
  - Edge-cases & direction-based scenarios  
  - Non-Vaasthu: "2+2?", "Write Python code", multilingual prompts  
- **Feedback Collection**:
  - In-person during meetups and hackathons  
  - WhatsApp messages and follow-up discussions  
- **Issues Raised**:
  1. Hallucinated answers  
  2. Inaccurate results from vector database  
  3. Non-Vaasthu queries handled poorly  
- **Fixes**:
  1. Added fallback logic  
  2. Finalized best prompt after 5 versions  
  3. Used chunk delimiters  
  4. Re-structured dataset for optimal retrieval

---

### 6. PROJECT LIFECYCLE & ROADMAP:

### Week 1: Development
- Finalized prompt and fallback architecture  
- Collected 350+ granular Vaasthu rules  
- Cross-verified all rules with Vaasthu Pandit: *Chandramouli Naroju (Gayithri Vaasthu Planners)*  
- Set up vector DB and upload logic  
- Integrated Groq + Qdrant + FastAPI  
- Created Bolt-based frontend  

### Week 2: Testing
- Resolved hallucination  
- Improved prompt format  
- Fixed routing logic for unknown queries

### Weeks 3–4: User Growth
- **Audience**: Architects, builders, spiritual planners  
- **Channels**: WhatsApp, LinkedIn, meetups  
- **Strategy**:
  - Encourage users to submit 5 queries  
  - Analyze logs for corpus growth

**Metrics**:
- 20+ local testers  
- 350+ structured Vaasthu rules verified

---

### 7. POST INTERNSHIP VISION:
- **Next Features**:
  - Auto-generate 2D floor plan designs according to vaasthu.
  - Generting Vaasthu validation report on uploading the 2D floor plans in website. 
  - Voice input & multilingual support
    
- **Long-term Goal**:
  - Make it easy for *every individual* to build homes filled with positive energy — creating **harmonious living spaces** backed by Vaasthu
 
- **Scaling Strategy**:
  - Fine-tune on collected logs  
  - Add LangGraph-based agents  
  - Grow dataset through community contributions
    
- **Sustainability**:
  - Keep active via open-source commits and social engagement  
  - Convert into a freemium SaaS tool for Vaasthu consultations

