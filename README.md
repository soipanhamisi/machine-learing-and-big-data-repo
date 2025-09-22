# Machine Learning and Big Data Repo

This repository contains a couple of beginner-friendly notebooks that demonstrate core scientific Python tooling and a simple machine learning workflow using scikit-learn.

Contents
- basics.ipynb: Quick tour of NumPy arrays, SciPy sparse matrices, and Matplotlib version check.
- classifying-iris-species.ipynb: An end-to-end example on the classic Iris dataset, including dataset inspection, train/test split, visualization, training a K-Nearest Neighbors classifier, prediction, and accuracy evaluation.

Prerequisites
- Python 3.9 or newer is recommended
- A working C compiler is not required (all dependencies are available as wheels on major platforms)

Key Python packages used
- numpy
- scipy
- matplotlib
- pandas
- scikit-learn
- mglearn (utility package from "Introduction to Machine Learning with Python")

Getting started
1) Clone or download this repository
   C:\Users\Admin\Documents\machine learing and big data repo

2) Create and activate a virtual environment (recommended)
- Using venv (built-in):
  - py -3 -m venv .venv
  - .venv\Scripts\activate

- Using conda (alternative):
  - conda create -n ml-basics python=3.11
  - conda activate ml-basics

3) Install dependencies
- With pip
  - pip install -U pip
  - pip install numpy scipy matplotlib pandas scikit-learn mglearn

- With conda
  - conda install numpy scipy matplotlib pandas scikit-learn
  - pip install mglearn

Note: mglearn is published on PyPI but may not be available via conda; install it with pip even in a conda environment.

Running the notebooks
You can use any of the following options:
- Jupyter Lab/Notebook
  - pip install jupyterlab
  - jupyter lab
  - Open basics.ipynb or classifying-iris-species.ipynb and run cells top-to-bottom.

- VS Code with the Python extension
  - Open the project folder in VS Code
  - Select your virtual environment as the interpreter
  - Open a notebook and run cells. The #%% cell markers in the files are also compatible with Python Interactive.

- PyCharm (Scientific Mode)
  - Open the project in PyCharm
  - Enable Scientific Mode and run cells or the entire notebook.

What the notebooks do
- basics.ipynb
  - Prints versions of NumPy and Matplotlib
  - Creates dense and sparse identity matrices (CSR and COO) and prints their representations

- classifying-iris-species.ipynb
  - Loads the Iris dataset and prints its keys, description snippet, feature and target names
  - Splits data into training and test sets using train_test_split
  - Visualizes feature relationships with pandas.plotting.scatter_matrix and mglearn color map
  - Trains a KNeighborsClassifier (k=1)
  - Makes a sample prediction and maps the predicted class index to a species name
  - Evaluates accuracy on the test set (prints mean accuracy and knn.score)

Reproducibility notes
- The train_test_split uses random_state=0 to ensure reproducible splits.
- Exact numeric outputs (e.g., accuracy) may vary if you change package versions, the random_state, or k neighbors.

Troubleshooting
- ImportError: No module named mglearn
  - Ensure you installed mglearn: pip install mglearn

- Backend/plotting issues in headless environments
  - If running without a display (e.g., a server), consider using Jupyter and avoid showing plots interactively.

- Package version mismatches
  - Update core libraries: pip install -U numpy scipy matplotlib pandas scikit-learn mglearn

License
- No explicit license has been provided in this repository. If you plan to use or distribute this code, consider adding a LICENSE file.

Acknowledgements
- The Iris dataset is provided by scikit-learn. The mglearn utilities are from the book "Introduction to Machine Learning with Python" by Andreas C. Müller and Sarah Guido.
