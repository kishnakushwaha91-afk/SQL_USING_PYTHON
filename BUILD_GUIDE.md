# 🚀 Build Guide

Welcome! This guide will help you set up and run the Python + SQL Lab Exercise.

## 📋 Prerequisites

Before we begin, ensure you have:
*   🐍 **Python 3.8+** installed.
*   📦 **pip** package manager ready.

---

## ⚙️ Installation

### 1. 📥 Clone & Navigate
If you haven't already:
```bash
git clone <repository-url>
cd <project-folder>
```

### 2. 🛡️ Virtual Environment (Recommended)
Keep your dependencies clean:
```bash
# Create venv
python3 -m venv venv

# Activate (Mac/Linux)
source venv/bin/activate

# Activate (Windows)
venv\Scripts\activate
```

### 3. 📦 Install Dependencies
We have a handy `requirements.txt` for you:
```bash
pip install -r requirements.txt
```

---

## 🏃‍♂️ Execution

### Jupyter Notebook 📓
This project is designed to run interactively in a Jupyter Notebook.

1.  Launch Jupyter:
    ```bash
    jupyter notebook
    ```
2.  Open `Python_SQL_Lab_Exercise_9.ipynb`.
3.  ⏩ Run all cells to see the database creation, data insertion, and query results!

---

## 🧐 Understanding the Output

| Output | What to look for |
| :--- | :--- |
| **Database Creation** 🏗️ | No errors when running the `sqlite3.connect` and `CREATE TABLE` cells. |
| **Data Insertion** 📝 | Successful execution of `INSERT` statements. |
| **Query Results** 🔍 | Tables or lists of data printed below each SQL query cell (e.g., list of clients, filtered orders). |

## 🆘 Troubleshooting

*   **Database Locked?** If you restart the kernel, make sure to close the connection properly or delete the `sales.db` file to start fresh.
*   **Module Not Found?** Ensure you activated your virtual environment before running `jupyter notebook`.
