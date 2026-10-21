# Jupyter-Notebook
Machine Learning and NLP practice notebook
Iris Flower Classification
A beginner-friendly machine learning project built in Jupyter Notebook to classify an iris flower into one of three species using four flower measurements. The notebook explores the dataset, visualizes feature relationships, trains two classification models, and evaluates their performance.
Project Overview
The project uses the Iris dataset available through scikit-learn. Each sample contains four numerical features:
- Sepal length (cm)
- Sepal width (cm)
- Petal length (cm)
- Petal width (cm)
The target is the flower species:
- Setosa
- Versicolor
- Virginica
The notebook compares two supervised classification algorithms:
1. Logistic Regression
2. K-Nearest Neighbors (KNN) with k=5 and feature standardization
Notebook
Main file: irispredict.ipynb

The notebook currently includes these stages:
1. Import Python libraries.
2. Load the built-in Iris dataset and create a pandas DataFrame.
3. Inspect missing values, data types, dataset dimensions, duplicates, and descriptive statistics.
4. Check the species distribution.
5. Visualize class counts, pairwise feature relationships, and feature distributions by species.
6. Split the data into training and testing sets (80% training, 20% testing) using random_state=42.
7. Train Logistic Regression and KNN models.
8. Evaluate both models using accuracy, classification reports, and confusion matrices.
9. Compare test accuracy and print the best-performing model.
Results
The notebook's saved evaluation output reports the following test results:
Model	Test accuracy in saved output
Logistic Regression	100%
K-Nearest Neighbors (KNN, k=5)	100%


The saved output identifies Logistic Regression as the best-performing model because it is listed first when both models have the same accuracy.

Important: The notebook file contains a mismatch between some current code cells and their saved outputs. For example, the current code loads sklearn.datasets.load_iris() and uses column names such as sepal length (cm), while some saved outputs show columns such as SepalLengthCm and Species values like Iris-setosa. Therefore, treat the results above as the results currently displayed in the notebook, not as independently verified results from a fresh run. Before publishing or submitting the project, restart the notebook kernel and run Run All Cells, then update this README with the refreshed output.
Tech Stack
- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
Requirements
Recommended Python environment: Python 3.10 or newer.

Install the required packages with:
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
If you use Jupyter Notebook already, you may only need to install the packages missing from your active notebook environment.
How to Run
1. Clone or download the project
If the notebook is in a Git repository, clone it and move into the project folder:
git clone <your-repository-url>
cd <your-project-folder>
Replace the placeholders with your actual repository URL and folder name. If you have only the notebook file, save irispredict.ipynb in a folder and open a terminal in that folder.
2. Create and activate a virtual environment (optional but recommended)
On Windows PowerShell:
py -m venv .venv
.\.venv\Scripts\Activate.ps1
3. Install dependencies
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
4. Start Jupyter Notebook
python -m notebook
Open irispredict.ipynb in the browser.
5. Refresh the notebook outputs
In Jupyter, select Kernel → Restart Kernel and Run All Cells (menu wording may vary). Confirm that every cell runs successfully and that the output columns and species labels match the current code.
Model Evaluation
The notebook evaluates models on a held-out test set with 30 samples. It uses:
- Accuracy to measure the proportion of correct predictions.
- Precision, recall, and F1-score to assess class-wise performance.
- Confusion matrices to show correct and incorrect predictions for each species.
KNN is placed inside a pipeline with StandardScaler, which standardizes the input features before classification. This is useful because KNN relies on distances between samples.
Limitations and Next Improvements
- The Iris dataset is small and commonly used for learning; results on it do not guarantee performance on other flower datasets.
- A single train/test split can produce optimistic results. Consider stratified cross-validation for a more robust comparison.
- Add a reusable prediction function that accepts four measurements and returns the predicted species.
- Save and load the selected model with joblib if you want to use it outside the notebook.
- Add input validation and a small interface only if you plan to turn the notebook into an application.
- Remove obsolete or unused code cells and rerun the notebook so that the code and saved outputs are consistent.
- The current Logistic Regression cell uses multi_class='multinomial', which produces a deprecation warning in newer scikit-learn versions. You can omit that argument and allow the library default to apply.
Project Structure
project-folder/
├── irispredict.ipynb
├── README.md
└── requirements.txt   # optional; can be added to pin dependencies
Learning Outcomes
By working through this project, you practice:
- Loading and inspecting a dataset
- Exploratory data analysis (EDA)
- Data visualization
- Training/testing data splitting
- Training classification models
- Evaluating classification performance
- Comparing multiple machine learning algorithm
