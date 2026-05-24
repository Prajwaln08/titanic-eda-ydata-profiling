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
git clone git@github.com:Prajwaln08/titanic-eda-ydata-profiling.git
cd titanic-eda-ydata-profiling
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

Generate a token at: **Settings → Developer settings → Personal access tokens → Tokens (classic)**  
Scopes needed: `repo` (full control). Public datasets work without a token.

### SSH setup (for contributors)

This repo uses SSH for git operations. If you're cloning to push changes:

```bash
# Generate a key (skip if you already have one)
ssh-keygen -t ed25519 -C "your@email.com" -f ~/.ssh/github_key

# Add to GitHub: Settings → SSH and GPG keys → New SSH key
cat ~/.ssh/github_key.pub

# Add to ~/.ssh/config
echo "Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/github_key
  IdentitiesOnly yes" >> ~/.ssh/config

# Test
ssh -T git@github.com
```

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
