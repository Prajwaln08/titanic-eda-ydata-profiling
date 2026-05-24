# Titanic EDA — YData Profiling

Exploratory Data Analysis of the Titanic dataset using **YData Profiling** (formerly pandas-profiling).
Dataset sourced from [HarshvardhanSingh-13/Datasets](https://github.com/HarshvardhanSingh-13/Datasets).

---

## Project Structure

```
.
├── titanic_eda_profiling.ipynb   # Main EDA notebook
├── requirements.txt              # Python dependencies
├── .env.example                  # Environment variable template
├── .env                          # Your local env vars (git-ignored)
└── README.md
```

---

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate        # macOS / Linux
# .venv\Scripts\activate         # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

```bash
cp .env.example .env
# Open .env and fill in your GITHUB_USERNAME and GITHUB_TOKEN
```

Generate a GitHub token at: **Settings → Developer settings → Personal access tokens → Fine-grained tokens**
Scopes needed: `Contents: Read-only` (public repos need no token).

### 5. Run the notebook

```bash
jupyter notebook titanic_eda_profiling.ipynb
```

---

## What the Notebook Does

| Step | Description |
|------|-------------|
| 1 | Setup & imports |
| 2 | Load environment variables from `.env` |
| 3 | Download Titanic dataset from GitHub |
| 4 | Data overview — shape, dtypes, sample rows |
| 5 | Missing values analysis |
| 6 | YData Profiling — full automated EDA report |
| 7 | Export report as `titanic_profile_report.html` |

---

## Dataset

- **Source**: [Titanic-Dataset.csv](https://github.com/HarshvardhanSingh-13/Datasets/tree/main/Titanic_Dataset)
- **Rows**: ~891 passengers
- **Key columns**: `Survived`, `Pclass`, `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`

---

## Author

**Prajwal Nerkar** — [prajwalnerkar01@gmail.com](mailto:prajwalnerkar01@gmail.com)
