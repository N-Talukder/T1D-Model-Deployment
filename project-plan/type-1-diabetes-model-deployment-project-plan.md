## T1D Model Deployment

### **Overview:**

This project aims to develop an interactive tool that demonstrates how machine learning (ML) models can be deployed in ways that _enhance user understanding, provide contextual transparency, and build trust through interpretability and interactivity_.

By integrating explainable AI (XAI) techniques and visual analytics, the tool will showcase how ML-driven insights can support clinical decision-making and public education around Type 1 Diabetes (T1D).

### **Intended Use Cases**

#### 1. For Clinical Practitioners

- **Goal:** Enable the design of **tailored and effective treatment strategies** for managing **T1D**, supported by interpretable ML models.
- **Key Features:**
  - Present ML-based recommendations with **transparent explanations** derived from user inputs.
  - Integrate **interactive visualizations** to highlight **key predictors** and their **influence on outcomes**, dynamically adapting to input data.
  - Promote **trust in AI-assisted care** by clearly illustrating the reasoning behind model predictions.

#### 2. For General Users

- **Goal:** Improve public **understanding of T1D** and **accessibility of ML concepts**.
- **Key Features:**
  - Offer an **educational interface** that visualizes the most important predictors of T1D identified by our models.
  - Explain, at a high level, how ML models generate predictions.
  - Demonstrate **model interpretability**, showing how individual features impact outcomes—bridging the **knowledge gap** between AI systems and end users.

**Keywords**: T1D, Machine Learning, Explainable AI (XAI), Visual Analytics, Trustworthy AI, Human-Centered Design, Decision Support System.

## MVP feature list

## Tech stack

### **Frontend**

- **Framework:** Next.js (React + TailwindCSS)
  - Interactive visual analytics (via Nivo/Chart.js/React-chart.js/Plotly.js/D3.js)

### **Backend**

- **Framework:** FastAPI
- **Libraries:** Scikit-learn (modeling), SHAP (explainability)

### **Project Management & Deployment**

- **Version Control & Management:** Git + GitHub
  - Issues, Tasks, Milestones, etc.
- **Deployment:** Vercel (Frontend) and Render (Backend)
- **Code Quality:**
  - ESLint, Prettier, and JSDoc for consistency and maintainability
  - - Supertest, Vitest

## Backend

### Endpoints

## Frontend

### UI Pages

| Page | Description |
| ---- | ----------- |

### UI Mockup

### Core UI Components

## Repository structure

```bash
 /root
 │
 ├── backend/
 │   ├── app/
 │   │   ├── routers/
 │   │   ├── models/
 │   │   ├── middleware/
 │   │   ├── core/
 │   │   ├── trained-models/
 │   │   ├── validators/
 │   │   └── utils/
 │   └── static/
 │   └── tests/
 │   └── dependencies.txt
 │   └── Dockerfile
 |
 ├── frontend/
 │   ├── app/
 │   ├── ├── _utilities/
 │   ├── ├── ├── backend-requests/
 │   ├── ├── ├── components/
 │   ├── ├── ├── hooks/
 │   ├── ├── ├── types/
 │   ├── ├── page1/
 │   ├── ├── page2/
 │   ├── ├── page3/
 │   ├── ├── page4/
 │   ├── public/
 │   ├── |── assets/
 │   ├── theme/
 │   ├── Dockerfile
 │
 ├── project-plan/
 │   ├── assets/
 │   ├── type-1-diabetes-model-deployment-project-plan.md
 │
 ├── docker-compose.yml
 ├── .gitignore
 ├── README.md
 └── LICENSE
```

## Optional Extra features (future)
