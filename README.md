# 30-Minute Skill Assessment: Virtual Environments, NumPy & Git Workflow

**Student Roll Number:** `pu02324eugbtcs097`  
**GitHub Username:** `suyashsharma097`  
**Repository:** [https://github.com/suyashsharma097/numpy-eval-pu02324eugbtcs097-.git](https://github.com/suyashsharma097/numpy-eval-pu02324eugbtcs097-.git)

---

## 📌 Assessment Overview

This repository contains the complete solution for the 30-Minute Skill Assessment covering:
1. Python Virtual Environment isolation and dependency management (`venv`).
2. Git version control, `.gitignore` rules, feature branching (`feature/matrix-multiply`), and non-fast-forward merges into `main`.
3. NumPy matrix generation, dimension validation using assertions, matrix multiplication ($\mathbf{C} = \mathbf{A} \cdot \mathbf{B}$), and matrix reductions (total sum, row-wise sums, column-wise sums) inside `matrix_ops.ipynb`.

---

## 📁 Repository Structure

```text
numpy_eval_pu02324eugbtcs097/
├── .gitignore              # Configured to exclude venv/, __pycache__/, .ipynb_checkpoints/
├── README.md               # Assessment documentation
├── matrix_ops.ipynb        # Jupyter notebook with executed code cell outputs
└── numpy_eval_pu02324eugbtcs097_assessment_report.pdf # PDF assessment report
```

---

## ⚙️ Virtual Environment Setup

To reproduce the environment and run the notebook locally:

```bash
# 1. Clone the repository
git clone https://github.com/suyashsharma097/numpy-eval-pu02324eugbtcs097-.git
cd numpy-eval-pu02324eugbtcs097-

# 2. Create and activate a Python virtual environment
python -m venv venv
# On Windows PowerShell:
.\venv\Scripts\Activate.ps1
# On Linux/macOS:
source venv/bin/activate

# 3. Install required packages
pip install numpy jupyter ipykernel nbformat
```

---

## 📊 NumPy Operations Breakdown (`matrix_ops.ipynb`)

### 1. Reproducibility & Matrix Generation
- **Random Seed:** Set to `42` (`np.random.seed(42)`).
- **Matrix A:** Shape `(4, 3)` with random integers in range `[1, 10]`.
- **Matrix B:** Shape `(3, 5)` with random integers in range `[1, 10]`.

```python
A = [[ 7,  4,  8],
     [ 5,  7, 10],
     [ 3,  7,  8],
     [ 5,  4,  8]]  # Shape: (4, 3)

B = [[ 8,  3,  6,  5,  2],
     [ 8,  6,  2,  5,  1],
     [10,  6,  9,  1, 10]] # Shape: (3, 5)
```

### 2. Dimension Validation & Matrix Multiplication
- **Assertion Validation:**
  ```python
  assert A.shape[1] == B.shape[0]  # Validates inner dimensions (3 == 3)
  ```
- **Matrix Dot Product ($C = A \cdot B$):**
  ```python
  C = np.dot(A, B)  # Resulting Matrix C Shape: (4, 5)
  ```
- **Matrix C Result:**
  ```text
  [[168,  93, 122,  63,  98],
   [196, 117, 134,  70, 117],
   [160,  99, 104,  58,  93],
   [152,  87, 110,  53,  94]]
  ```

### 3. Reductions & Summary Statistics
- **Total Sum ($\sum_i \sum_j C_{ij}$):** `2188`
- **Row-wise Sums (`axis=1`):** `[544, 634, 514, 496]`
- **Column-wise Sums (`axis=0`):** `[676, 396, 470, 244, 402]`

---

## 🔀 Git Branching & Merge History

The Git repository contains a multi-branch commit history:

```text
*   cced56c Merge branch 'feature/matrix-multiply' into main (main, origin/main)
|\  
| * 5c8a6ba feat: implement random matrix creation and dot multiplication (feature/matrix-multiply, origin/feature/matrix-multiply)
|/  
* 272b37f Initial commit: project structure and gitignore
```

- **Branch `feature/matrix-multiply`**: Contains the matrix implementation commit.
- **Branch `main`**: Merged feature branch via explicit merge commit.
