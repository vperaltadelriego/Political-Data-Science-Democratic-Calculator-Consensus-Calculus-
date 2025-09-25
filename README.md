# PoliticalDataScience (PDS)
A library to do political data science, social choice applied theory and in general collective choice applied theory 

## 📊 Overview

**PoliticalDataScience (PDS)** is a Python library designed for advanced analysis and simulation of political preferences and voting systems. It allows researchers, data scientists, and political analysts to apply various voting methods—from traditional plurality to sophisticated preferential and score-based systems—to structured data, incorporating complex parameters like voter weight, issue relationships, and semantic interpretation.

PDS is an ideal tool for exploring voter behavior, identifying potential paradoxes (like Condorcet cycles), and comparing the theoretical results of different election models.

---

## ✨ Features

* **Diverse Voting Systems:** Implements Plurality, Approval, Borda Count, Ranked-Choice (Instant-Runoff), and Condorcet methods.
* **Advanced Scoring:** Includes Borda-style scoring and Olympic Appreciation (eliminating extreme scores).
* **Semantic Interpretation:** Includes a `semantics` parameter to analyze preferences based on three logical models: `standard`, `exclusionary`, and `open_world`.
* **Customizable Parameters:** Supports voter weights, open/closed scales, and user-defined option relationships for nuanced analysis.
* **Diagnostics:** Functions to detect invalid voters (multiple votes) and calculate option profitability.

---

## 🚀 Installation

As this is a new library, you will clone the repository for now. Once the project is uploaded to PyPI, the installation method will change to `pip`.

### Prerequisites

You must have **Python 3.8+** installed.

### Current Installation (From Source)

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YourUsername/political-data-science.git](https://github.com/YourUsername/political-data-science.git)
    cd political-data-science
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *Note: This currently installs `pandas` and `numpy`.*

---

## 🛠️ Quick Start

### 1. Prepare Your Data

Your data must be in a Pandas DataFrame format. The example below uses a simple dataset.

```python
import pandas as pd
from political_data_science.core import PoliticalDataScience

data = {
    'voter_id': [1, 2, 3, 4],
    'name': ['Juan', 'Pedro', 'Luis', 'Julián'],
    'weight': [3, 1, 3, 10],
    'ballot': ['vanilla', 'vanilla', 'chocolate', 'fresa']
}
df = pd.DataFrame(data)
