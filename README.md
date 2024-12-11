# git_assignment_HeroVired



# Git Assignment: Hero Vired

## Title: CalculatorPlus & GeometryCalculator

### Description:
This repository contains two Python applications:

1. **CalculatorPlus**: A simple calculator that supports basic arithmetic operations and square root calculations.
2. **GeometryCalculator**: A utility to calculate areas of circles and rectangles.

Both applications demonstrate branching, merging, and stashing techniques in Git, along with Git LFS usage for large binary files.

---

### **Features:**

#### **CalculatorPlus**:
- Addition
- Subtraction
- Multiplication
- Division with error handling
- Square root calculation

#### **GeometryCalculator**:
- Calculate the area of a circle
- Calculate the area of a rectangle

---

### **Git Techniques:**

- **Branching**: Work on different features in isolated branches.
- **Merging**: Integrate completed features back into the main branch.
- **Stashing**: Temporarily save unfinished work to switch branches without losing progress.
- **Git LFS**: Efficiently manage large binary files.

---

### **Prerequisites:**
1. Python 3.x installed
2. Git installed
3. GitHub account with access to create private repositories
4. **Git LFS** installed (for large files)

---

### **Requirements:**

#### **Python Libraries:**
- `math` (standard Python library)

#### **GitHub CLI (Optional):**
- Useful for easier GitHub operations.

---

### **Using the Program:**

#### **1. CalculatorPlus**:
##### **Commands:**

- Clone the repository:
  ```bash
  git clone <repository-link>
  cd git_assignment_HeroVired
  ```

- Switch to the `dev` branch:
  ```bash
  git checkout dev
  ```

- Run the `CalculatorPlus.py` app:
  ```bash
  python CalculatorPlus.py
  ```

##### **Sample Input & Output:**
```
16 + 4 = 20
16 - 4 = 12
16 * 4 = 64
16 / 4 = 4.0
The square root of 25 = 5.0
```

---

#### **2. GeometryCalculator**:
##### **Commands:**

- Switch to the `geometry-calculator` branch:
  ```bash
  git checkout geometry-calculator
  ```

- Run the `GeometryCalculator.py` app:
  ```bash
  python GeometryCalculator.py
  ```

##### **Sample Input & Output:**
```
The area of the circle with radius 5 = 78.54
The area of the rectangle with length 10 and width 6 = 60
```

---

### **Git Workflow:**

#### **1. Create Repository and Branches:**
Initialize Git and create the `dev` branch:
```bash
git init
git remote add origin <repository-link>
git checkout -b dev
```

#### **2. Add and Commit Files:**
Add your initial files and commit:
```bash
git add .
git commit -m "Initial commit for CalculatorPlus"
```

#### **3. Create and Merge Feature Branch:**
Create a feature branch to implement the square root functionality:
```bash
git checkout -b feature/sqrt
# Implement and commit square root feature
git add CalculatorPlus.py
git commit -m "Added square root functionality"
```

Merge the feature back into the `dev` branch:
```bash
git checkout dev
git merge feature/sqrt
```

#### **4. Bug Fix in Division:**
Create a hotfix branch for fixing the divide-by-zero bug:
```bash
git checkout -b hotfix/divide
# Fix divide by zero error
git add CalculatorPlus.py
git commit -m "Fixed division by zero bug"
```

Merge the hotfix back into `dev`:
```bash
git checkout dev
git merge hotfix/divide
```

#### **5. Use Git LFS:**
If you need to manage large binary files (e.g., `.bin` files), follow these steps:

- Install Git LFS:
  ```bash
  git lfs install
  ```

- Create an `lfs` branch:
  ```bash
  git checkout -b lfs
  ```

- Track large files (e.g., `.bin` files):
  ```bash
  git lfs track "*.bin"
  echo "*.bin" >> .gitattributes
  ```

- Add the large file:
  ```bash
  git add .gitattributes large_file.bin
  git commit -m "Added large file with Git LFS"
  git push origin lfs
  ```

#### **6. Use Git Stash:**
Stash unfinished work to switch branches:
- For Circle Area feature:
  ```bash
  git checkout -b feature/circle-area
  # Stash your progress
  git stash
  ```

- Switch to the Rectangle Area feature:
  ```bash
  git checkout -b feature/rectangle-area
  # Apply stashed changes
  git stash apply
  ```

---

### **Final Steps:**

#### **1. Create Pull Requests:**
- After finishing both features (`circle-area` and `rectangle-area`), create pull requests to the `dev` branch on GitHub.

#### **2. Review and Merge:**
- Request a code review from a team member.
- After receiving approval, merge both pull requests into the `dev` branch.

#### **3. Testing and Merge to Main:**
- Once the features are tested and validated in the `dev` branch, merge them into the `main` branch:
  ```bash
  git checkout main
  git merge dev
  ```

#### **4. Version Release:**
- Tag the release for version 1 or version 2 depending on your development cycle:
  ```bash
  git tag -a v2.0 -m "Version 2 release"
  git push origin v2.0
  ```

---

### **GitHub Repository Overview:**
- **Repository Name:** `git_assignment_HeroVired`
- **Branches:**
  - `dev`: The development branch.
  - `geometry-calculator`: Branch for GeometryCalculator functionality.
  - `feature/sqrt`: Branch for implementing the square root feature in CalculatorPlus.
  - `hotfix/divide`: Branch for fixing the divide by zero bug.
  - `lfs`: Branch for managing large binary files using Git LFS.
  
---

### **Important Notes:**
- Make sure to have **Git LFS** installed for large files (over 200MB) such as videos, large datasets, etc.
- **Git Stash** is useful when you need to switch branches without losing your current progress.
- Always verify changes in a **feature branch** before merging them into the **main** or **dev** branches.
```

---

This Markdown file covers all the necessary steps and instructions, formatted for easy reading and use in GitHub or any Markdown viewer.
