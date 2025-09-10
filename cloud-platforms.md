# Google Colab & Kaggle Quick Start Guide

## Google Colab

### What is it?
Free cloud-based Jupyter notebooks with GPU access. No installation needed.

### Getting Started
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Sign in with your Google account
3. Click **"New notebook"**
4. Start coding immediately!

### Basic Usage
- **Run code**: Press `Shift + Enter`
- **Add code cell**: Click `+ Code`
- **Add text cell**: Click `+ Text`
- **Save**: `Ctrl + S` (auto-saves to Google Drive)

### Essential Commands
```python
# Install packages
!pip install package_name

# Upload files
from google.colab import files
uploaded = files.upload()

# Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')

# Download files
files.download('filename.csv')
```

### Free GPU Access
1. Go to **Runtime** → **Change runtime type**
2. Select **GPU** under Hardware accelerator
3. Click **Save**

---

## Kaggle

### What is it?
Data science platform with free datasets, notebooks, and competitions.

### Getting Started
1. Go to [kaggle.com](https://kaggle.com)
2. Create free account
3. Verify with phone number
4. Start exploring datasets or competitions

### Using Kaggle Notebooks
1. Go to **Code** tab
2. Click **New Notebook**
3. Choose **Notebook** or **Script**
4. Start coding with pre-loaded datasets

### Key Features
- **Datasets**: Click **Datasets** to browse
- **Competitions**: Join challenges for practice
- **Free GPU/TPU**: 30 hours/week limit
- **Community**: Learn from other notebooks

### Essential Tips
```python
# Access competition data
import os
for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename))

# Download datasets
!kaggle datasets download -d dataset-name
```

---

## Quick Comparison

| Feature | Google Colab | Kaggle |
|---------|-------------|---------|
| **Setup** | Instant | Instant |
| **Storage** | Google Drive | Built-in datasets |
| **GPU** | Free (limited) | Free 30h/week |
| **Best for** | Learning, prototyping | Data competitions, practice |

## When to Use What?

**Use Google Colab when:**
- Learning Python basics
- Working with your own data
- Need Google Drive integration

**Use Kaggle when:**
- Want practice datasets
- Learning data science
- Joining competitions

---

*Both platforms are free and perfect for learning Python without local setup!*