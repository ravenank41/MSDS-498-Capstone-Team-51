Repo currently holds the following primary folders:
- app: front-end applications
- data: data lake & versioned artifacts
- notebooks: exploratory & prototyping notebooks
- rag: hybrid structured + semantic RAG module
- src: production source code (Python/R)
- tests: unit tests for various purposes

Repo also contains the following root directory files:
- requirements.txt: dependencies
- .gitignore: excludes unnecessary local files during commits

Below is an example layout for the full repo as the project progresses\
MSDS-498-Capstone-Team-51/\
│\
├── data/                      # Data Lake & Versioned Artifacts\
│   ├── raw/                   # Immutable raw scrapes (HTML cache, CSVs)\
│   ├── processed/             # Cleaned relational outputs (player_season_master.csv)\
│   └── exports/               # Final model predictions & team cap sheets\
│\
├── notebooks/                 # Exploratory & Prototyping Jupyter / R Notebooks\
│   ├── 01_eda_clustering.ipynb\
│   ├── 02_aging_model.ipynb\
│   └── 03_fair_pay_bakeoff.ipynb\
│\
├── src/                       # Production Python Source Code (Modular Scripts)\
│   ├── __init__.py\
│   ├── data_pipeline.py       # Automated ingestion, cleaning, and joining\
│   ├── features.py            # Feature engineering (rolling stats, durability)\
│   ├── aging_model.py         # Recency-anchor + age curve projection engine\
│   ├── fair_pay_model.py      # CensoredRegressor & CBA max/min post-processing\
│   ├── cap_simulator.py       # 4-year 30-team payroll & apron penalty engine\
│   └── decision_engine.py     # Extend / Hold / Trade / Let Walk logic\
│\
├── rag_chatbot/               # Hybrid Structured + Semantic RAG Module\
│   ├── vector_db/             # Local vector store (ChromaDB / FAISS)\
│   ├── documents/             # Markdown chunks of 2023 CBA rules & player cards\
│   └── agent.py               # SQL/Pandas tool-router + LLM orchestration\
│\
├── app/                       # Front-End Applications\
│   ├── streamlit_app/         # Mobile/Web lookup app & chat interface\
│   └── shiny_or_tableau/      # Executive dashboard files\
│\
├── tests/                     # Unit tests for data joins, CBA clamps, and models\
├── requirements.txt           # Python dependencies (pandas, scikit-learn, etc.)\
├── README.md                  # Project charter, architecture, and run instructions\
└── .gitignore                 # Exclude cache dirs, local keys, and raw HTML
