# UNBench


## Overview

This project provides tools for analyzing, simulating, and generating content related to United Nations Security Council (UNSC) draft resolutions using language models. The tasks involve coauthor selection, voting simulation, resolution adoption prediction, and statement generation. We released approximately 30 samples for each task, and the full dataset will be made publicly available upon the paper's acceptance.

## Features

- **Task 1:** Coauthor selection for UNSC draft resolutions.
- **Task 2:** Simulate country voting behavior on draft resolutions.
- **Task 3:** Predict the adoption of UNSC draft resolutions.
- **Task 4:** Generate diplomatic statements for UNSC meetings.

## Tasks Breakdown

### Task 1 - Coauthor Selection
- **Goal:** Choose the most suitable coauthor for a UNSC draft resolution.
- **Input:** Draft resolutions and a list of potential coauthors.
- **Output:** Selected coauthor per draft.

### Task 2 - Voting Simulation
- **Goal:** Simulate voting outcomes by different countries on draft resolutions.
- **Input:** Draft resolutions and country profiles.
- **Output:** Voting results (`Y` for Yes, `N` for No, `A` for Abstain) and evaluation metrics.

### Task 3 - Resolution Adoption Prediction
- **Goal:** Predict whether a draft resolution will be adopted.
- **Input:** Text of draft resolutions.
- **Output:** Binary classification (`1` for adopted, `0` for rejected) and model performance metrics.

### Task 4 - Diplomatic Statement Generation
- **Goal:** Generate representative statements for countries on draft resolutions.
- **Input:** Draft resolutions and country profiles.
- **Output:** Generated statements and ROUGE-L scores for evaluation.

## Project Structure

```
main/
│
├── run_task1.ipynb   # Task 1 - Coauthor selection
├── run_task2.ipynb   # Task 2 - Voting simulation
├── run_task3.ipynb   # Task 3 - Adoption prediction
├── run_task4.ipynb   # Task 4 - Statement generation
│
├── task1.json        # Data for Task 1
├── task2.csv         # Data for Task 2
├── task3.json        # Data for Task 3
├── task4.json        # Data for Task 4
│
├── task1/            # Directory containing draft resolution files for Task 1
└── task2/            # Directory containing draft resolution files for Task 2
```

## Installation

1. **Clone the repository:**

   ```bash
   git clone <repository_url>
   cd github_data
   ```

2. **Set up a virtual environment and install dependencies:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

3. **Add Together API credentials:**

   Replace placeholders in notebooks:

   ```python
   your_model_name = 'xxxxxxxxxxxxxxxxxxxxxxxx'
   your_api_key = 'xxxxxxxxxxxxxxxxxxxxxxxx'
   ```

   with your Together API details or you can use your own LLMs.

## Usage

1. **Launch Jupyter Notebooks:**

   ```bash
   jupyter notebook
   ```

2. **Run the desired task notebooks:**
   - `run_task1.ipynb` — Coauthor selection.
   - `run_task2.ipynb` — Voting simulation.
   - `run_task3.ipynb` — Adoption prediction.
   - `run_task4.ipynb` — Statement generation.

3. **Evaluate model outputs:**
   - Tasks 2 & 3 include performance metrics like Accuracy, AUC, F1 Score, and others.
   - Task 4 computes ROUGE-L scores for generated statements.

## Requirements

- Python 3.x
- Jupyter Notebook
- together
- pandas
- numpy
- scikit-learn
- tqdm
- imbalanced-learn
- rouge-score

