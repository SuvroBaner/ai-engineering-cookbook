## 🦜
# __LangGraph Essentials__

This repository will cover an introduction to key LangGraph concepts: State, Nodes, Edges, Memory, and Interrupts. 
The final notebook will demonstrate how to build a production-style email support workflow.

## 🚀 Setup 

### Prerequisites

- Ensure you're using Python 3.11 - 3.13.
- [uv](https://docs.astral.sh/uv/) package manager or [pip](https://pypi.org/project/pip/)
- OpenAI API key

### Installation

Download the course repository

```bash
# Clone the repo, cd to 'python' directory
git clone https://github.com/SuvroBaner/ai-engineering-cookbook.git
cd ./langgraph/essentials/
```

Make a copy of example.env

```bash
# Create .env file
cp example.env .env
```

Insert API keys directly into .env file, OpenAI (required) and [LangSmith](#getting-started-with-langsmith) (optional)

```bash
# Add OpenAI API key
OPENAI_API_KEY=your_openai_api_key_here

# Optional API key for LangSmith tracing
LANGSMITH_API_KEY=your_langsmith_api_key_here
LANGSMITH_TRACING=true
LANGSMITH_PROJECT=langgraph-py-essentials
```

Make a virtual environment and install dependancies
```bash
# Create virtual environment and install dependancies
uv sync
```

Run notebooks

```bash
# Run Jupyter notebooks directly with uv
uv run jupyter lab

# Or activate the virtual environment if preferred
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
jupyter lab
```

Optional: Setup [LangSmith Studio](https://docs.langchain.com/oss/python/langchain/studio)

```bash
# copy the .env file you created above to the studio directory
cp .env ./studio/.

#to run
langgraph dev
```

### Getting Started with LangSmith

- Create a [LangSmith](https://smith.langchain.com/) account
- Create a LangSmith API key
<img width="1196" height="693" alt="Screenshot 2025-10-16 at 8 28 03 AM" src="https://github.com/user-attachments/assets/e39b8364-c3e3-4c75-a287-d9d4685caad5" />
<img width="1196" height="468" alt="Screenshot 2025-10-16 at 8 29 57 AM" src="https://github.com/user-attachments/assets/2e916b2d-e3b0-4c59-a178-c5818604b8fe" />



## 📚 Tutorial Overview

This repository contains notebooks langgraph essential concepts and showcasing an end-to-end email agent. This will enable you to build any workflow or agent.

### LangGraph Essentials Notebooks
- You will use all the components of LangGraph
    - State and Nodes
    - Edges
        - Parallel
        - Conditional
    - Memory
    - Interrupts/ Human-In-The-Loop  

### `application.ipynb` - Build A Email Support Workflow
Learn to implement structured workflow to process customer emails. This notebook utilizes all of the building blocks from the first notebook in an example application.:
- Task tracking with status management (pending/in_progress/completed)  
