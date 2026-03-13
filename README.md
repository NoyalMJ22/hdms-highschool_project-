<div align="center">

```
██╗  ██╗██████╗ ███╗   ███╗███████╗
██║  ██║██╔══██╗████╗ ████║██╔════╝
███████║██║  ██║██╔████╔██║███████╗
██╔══██║██║  ██║██║╚██╔╝██║╚════██║
██║  ██║██████╔╝██║ ╚═╝ ██║███████║
╚═╝  ╚═╝╚═════╝ ╚═╝     ╚═╝╚══════╝
```

### `High school Database Management System`
> *Class 12 Computer Science Project · Batch 2022–23*

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![Beta version](https://img.shields.io/badge/version-beta-tomato)](https://img.shields.io/badge/beta-version-tomato)
[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)](https://pandas.pydata.org)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557c)](https://matplotlib.org)
[![NumPy](https://img.shields.io/badge/NumPy-1.x-013243?logo=numpy)](https://numpy.org)

</div>

---

## 📌 Overview

**HDMS** is a command-line database management system built to display, compare, and analyse student data across **Classes 7 to 12** of a high school. It provides educators and administrators with visual comparisons between classes, while enforcing strict data privacy — contact details, addresses, and individual marks are never exposed.

```python
# Example usage
from hdms import StudentDatabase

db = StudentDatabase(classes=range(7, 13))
db.compare(metric="strength", visualise=True)
```

---

## 👨‍💻 Authors

| Name | Role |
|---|---|
| **Noyal Mathew Jain** | Developer |
| **Disni Sajeev** | Developer |
| **Amal Lalgi** | Developer |

---

## ⚙️ Tech Stack

```
hdms/
├── index.py              ← Entry point
├── database/
│   ├── students.csv      ← Raw student data
│   └── classes.csv       ← Class-level aggregates
├── modules/
│   ├── display.py        ← Pandas-powered table rendering
│   ├── compare.py        ← Cross-class comparison logic
│   └── visualise.py      ← Matplotlib/NumPy charting
└── utils/
    └── privacy.py        ← Data masking & access control
```

| Library | Purpose |
|---|---|
| `Python 3.x` | Core runtime — no frameworks, raw Python |
| `Pandas` | Data loading, filtering, and aggregation |
| `Matplotlib` | Bar charts, pie charts, and class comparisons |
| `NumPy` | Numerical computations and statistics |

---

## 🚀 Installation

**Prerequisites**

```bash
python --version   # Python 3.8 or higher required
```

**Step 1 — Install dependencies**

```bash
pip install pandas matplotlib numpy
```

**Step 2 — Clone the repository**

```bash
git clone https://github.com/your-repo/hdms.git
cd hdms
```

**Step 3 — Run the application**

```bash
python index.py
```

---

## 🔒 Privacy Policy

HDMS is designed with student safety as a priority:

- ✅ Class-level statistics and comparisons are publicly visible
- ✅ General strength/weakness analysis per class is available
- ❌ Individual student marks are **never** displayed
- ❌ Contact details (phone, email) are **masked**
- ❌ Home addresses are **not stored or shown**

```python
# privacy.py — how sensitive fields are handled
RESTRICTED_FIELDS = ["phone", "email", "address", "marks"]

def sanitise(record: dict) -> dict:
    return {k: v for k, v in record.items()
            if k not in RESTRICTED_FIELDS}
```

---

## 📊 Features

- **Class Comparison** — Compare Classes 7–12 side-by-side on academic and co-curricular metrics
- **Strength Analysis** — Identify top-performing areas per class using aggregated data
- **Visual Charts** — Bar charts, pie charts, and trend lines via Matplotlib
- **Secure by Default** — Sensitive fields are stripped before any data is rendered

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

```bash
# 1. Fork the repository
# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Commit your changes
git commit -m "feat: describe your change"

# 4. Push and open a Pull Request
git push origin feature/your-feature-name
```

> Please adhere to this project's `code of conduct` when contributing.

---

## 📄 License

```
MIT License — Copyright (c) 2023 Noyal Mathew Jain, Disni Sajeev, Amal Lalgi
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software...
```

See [`LICENSE`](LICENSE) for full terms.

---

<div align="center">
  <sub>Built with 🐍 Python · Class 12 CS · 2022–23</sub>
</div>
