# Study Group 16 - Fundamentals of Quantum Computing Using Qiskit v2.X Developer

## 📋 About this repository
 
This repository centralizes all notebooks, scripts, and notes produced during our weekly study sessions. The group meets **1–2 hours per week** over **12 weeks**, following a structured plan based on the official IBM Study Guide and Sample Test for Exam C1000-179.
 
---
 
## 👥 Group members
 
| Name | GitHub | Initial role |
|------|--------|--------------|
| Diogo    | —      | —            |
| Gabriel    | —      | —            |
| José Victor    | —      | —            |
| Pedro    | —      | —            |

## 🗂️ Repository structure
 
```
qiskit-study-group/
│
├── weeks/
│   ├── week-01/            # Section 1 — Pauli Operators + Quantum Gates
│   ├── week-02/            # Section 2 — Visualizing circuits and states
│   ├── week-03/            # Section 3 — Basic and dynamic circuits
│   ├── week-04/            # Section 3 — Parameterized circuits + transpilation
│   ├── week-05/            # Section 4 — Execution modes (Session/Batch)
│   ├── week-06/            # Section 4 — Primitives + Broadcasting Rules
│   ├── week-07/            # Section 5 — Sampler Primitive
│   ├── week-08/            # Section 6 — Estimator Primitive
│   ├── week-09/            # Sections 7+8 — Results + OpenQASM 3
│   ├── week-10/            # Full review + mock exam
│   ├── week-11/            # Final project
│   └── week-12/            # Final mock exam + certification
│
├── final-project/          # Group integrative notebook
├── resources/              # Links, cheatsheets, and general notes
└── README.md
```
 
Each `week-XX/` folder should contain:
- `notebook.ipynb` — session code
- `notes.md` — key takeaways, questions, and answers
- `sample_test_questions.md` — worked questions with commented answer key
 
---
 
## 🗓️ 12-week schedule
 
| Week | Phase | Exam section | Topic | Priority |
|------|-------|--------------|-------|----------|
| 1 | 1 | Section 1 (16%) | Pauli Operators + quantum gates | 🔴 High |
| 2 | 1 | Section 2 (11%) | Visualizing circuits, measurements, and states | 🟠 Medium-High |
| 3 | 1 | Section 3 (18%) | Basic and dynamic circuits | 🔴 Critical |
| 4 | 1 | Section 3 (18%) | Parameterized circuits + transpilation | 🔴 Critical |
| 5 | 2 | Section 4 (15%) | Execution modes: Session, Batch, Single Job | 🔴 High |
| 6 | 2 | Section 4 (15%) | Primitives + Broadcasting Rules + Jobs | 🔴 High |
| 7 | 2 | Section 5 (12%) | Sampler Primitive: options and theory | 🟠 Medium-High |
| 8 | 2 | Section 6 (12%) | Estimator Primitive: options and theory | 🟠 Medium-High |
| 9 | 3 | Sections 7+8 (16%) | Results, job monitoring + OpenQASM 3 | 🟡 Medium |
| 10 | 3 | Review | Partial mock exam — all 21 Sample Test questions | — |
| 11 | 3 | Final Project | Integrative notebook + weak spots reinforcement | — |
| 12 | 3 | 🎯 Exam | Final mock exam + Exam C1000-179 (Pearson VUE) | — |
 
---
 
## ⚙️ Environment setup
 
### Prerequisites
 
- Python 3.9+
- Free account on [IBM Quantum Platform](https://quantum.cloud.ibm.com)
 
### Installation
 
```bash
# Clone the repository
git clone https://github.com/<your-username>/qiskit-study-group.git
cd qiskit-study-group
 
# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate        # Linux/macOS
.venv\Scripts\activate           # Windows
 
# Install dependencies
pip install qiskit qiskit-ibm-runtime qiskit-aer jupyter matplotlib pylatexenc
```
 
### Configure IBM Quantum credentials
 
```python
from qiskit_ibm_runtime import QiskitRuntimeService
 
# Run once to save credentials locally
QiskitRuntimeService.save_account(
    channel="ibm_quantum",
    token="YOUR_TOKEN_HERE",  # Get it at quantum.cloud.ibm.com
    overwrite=True
)
```
 
> ⚠️ **Never commit your IBM Quantum token.** Use environment variables or the `save_account()` method above, which stores credentials locally on your machine.
 
---
 
## 🔐 Security
 
Add a `.gitignore` file at the root of the project to avoid exposing credentials:
 
```
.env
*.env
.venv/
__pycache__/
.ipynb_checkpoints/
*.pyc
```
 
---
 
## 📚 Study resources
 
| Resource | Link |
|----------|------|
| IBM Quantum Learning (official) | [learning.quantum.ibm.com](https://learning.quantum.ibm.com) |
| Qiskit Documentation | [quantum.cloud.ibm.com/docs](https://quantum.cloud.ibm.com/docs) |
| IBM Quantum Composer | [composer.quantum.ibm.com](https://composer.quantum.ibm.com) |
| Qiskit YouTube | [youtube.com/@qiskit](https://youtube.com/@qiskit) |
| OpenQASM 3 Reference | [openqasm.com](https://openqasm.com/versions/3.0/language/types.html) |
| Schedule exam (Pearson VUE) | [home.pearsonvue.com/ibm](https://home.pearsonvue.com/ibm) |
 
---
 
## 🤝 How to contribute
 
1. **Create a branch** named after the current week before each session:
   ```bash
   git checkout -b week-01
   ```
 
2. **Add your files** to the corresponding folder (`weeks/week-01/`)
 
3. **Open a Pull Request** to `main` after the session
 
4. **Another member reviews** before merging — this reinforces learning for both sides!
 
---
 
## ✅ Progress checklist
 
- [ ] Week 1 — Pauli Operators + quantum gates
- [ ] Week 2 — Visualization
- [ ] Week 3 — Basic and dynamic circuits
- [ ] Week 4 — Parameterized circuits + transpilation
- [ ] Week 5 — Execution modes
- [ ] Week 6 — Primitives + Broadcasting
- [ ] Week 7 — Sampler
- [ ] Week 8 — Estimator
- [ ] Week 9 — Results + OpenQASM
- [ ] Week 10 — Partial mock exam ≥70% ✓
- [ ] Week 11 — Final project presented
- [ ] Week 12 — 🏆 Exam C1000-179 completed
 
---