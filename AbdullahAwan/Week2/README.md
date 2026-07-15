# Week 2 - Internship Progress
## FlyRank AI Machine Learning Internship

---

## Assignment 2: Research Question Framing (Setup Phase)

**Objective:**
To define a clear research question — connecting the data, the decision 
it improves, the action someone takes, and the cost of getting it wrong 
— before starting any modeling work.

**Work Completed:**

1. Selected **"Refresh/Content Opportunity Scoring"** as my project lane 
   — identifying which content pages should be reviewed first.
2. Backed the lane choice with real data from the starter dataset: 
   over 13,000 pages (43.8%) showing genuine decline.
3. Referenced the 3x model improvement already proven in Assignment 1 
   as supporting evidence for the lane's value.
4. Documented the decision, the action, and the cost of a wrong 
   recommendation in the notebook's markdown cells.
5. Completed the notebook with supporting code cells showing the 
   real numbers used to justify the lane choice.
6. Committed the completed notebook to GitHub repository and 
   submitted on the assignment portal.

**Deliverable:** `work/notebooks/w01_research_question.ipynb`

---

## Assignment 3: ML Task Framing (Foundations Phase)

**Objective:**
To map the chosen project lane onto a formal ML task type, defining 
the target, success metric, and unit of analysis.

**Work Completed:**

1. Defined the project as a **Ranking/Scoring problem**.
2. Set the target variable as `is_declining_label`.
3. Chose **Precision@50** as the success metric.
4. Built a dataframe showing the unit of analysis (one row = one 
   content page).
5. Explained why this problem needs machine learning rather than a 
   simple fixed rule, using the model's proven 3x improvement as 
   evidence.
6. Committed the completed notebook to GitHub repository and 
   submitted on the assignment portal.

**Deliverable:** `work/notebooks/w02_ml_task_framing.ipynb`

---

**Files in this folder:**
- `w01_research_question.ipynb`
- `w02_ml_task_framing.ipynb`
  
