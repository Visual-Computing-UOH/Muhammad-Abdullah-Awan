
# Week 3 - Internship Progress
## FlyRank AI Machine Learning Internship

**Assignment:** Data Contract (Foundations Phase)

**Objective:**
To work directly with FlyRank's real warehouse data (hosted on Hugging 
Face, ~79 million rows) instead of the small starter dataset — 
describing the project lane's slice of the data pipeline, verifying it 
with real queries, building initial features, and demonstrating the 
data leakage trap.

**Work Completed:**

1. Wrote a data contract in plain words — defined the unit of analysis 
   (one content page per client per month), the tables used, the time 
   window, the target/proxy, and what was deliberately excluded 
   (private data, product-decision fields).

2. Verified the contract with three real database queries on live 
   warehouse data (month = March 2026):
   - **Grain check** — confirmed no duplicate rows
   - **Row count and date span check** — 9.8 million rows, 55 clients, 
     331,437 content items
   - **Availability check** — filtered with IS TRUE, confirmed 
     surviving row count

3. Built a five-feature data frame from real warehouse data, justifying 
   for each feature why it would be knowable at the decision moment.

4. Performed the deliberate "data leakage" experiment — added a 
   label-derived column, observed the quick score jump toward perfect, 
   then removed it to demonstrate the honest, correct approach.

5. Named one limitation of the data slice used.

**Deliverable:** `work/notebooks/w03_data_contract.ipynb`

**Files in this folder:**
- `w03_data_contract.ipynb`
  
