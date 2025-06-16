# Inside Out ML: Emotion Classification from fMRI

This repository contains the final project for CS 6140 Machine Learning, focusing on emotion classification from fMRI data using various parcellation and projection techniques. It explores feature extraction methods for high-dimensional, auto-correlated neuroimaging data in multi-class classification tasks.

---

## Getting Started

To set up the project and run the analysis, please follow these steps:

1.  **Clone the Repository:**
    Navigate to the project's dedicated branch and clone the repository:
    ```
    git clone [https://github.com/deepyaad/emotion-fmri-classification.git](https://github.com/deepyaad/emotion-fmri-classification.git) --branch cs6140 --single-branch
    ```

2.  **Navigate into the Project Directory:**
    ```
    cd emotion-fmri-classification
    ```

3.  **Create a Virtual Environment:**
    ```
    python -m venv venv
    ```

4.  **Activate the Virtual Environment:**
    * **On macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```
    * **On Windows (Command Prompt):**
        ```cmd
        .\venv\Scripts\activate.bat
        ```
    * **On Windows (PowerShell):**
        ```powershell
        .\venv\Scripts\Activate.ps1
        ```

5.  **Install Required Packages:**
    Install all necessary Python libraries listed in `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

6.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    This command will open a browser window displaying the project directory.

---

## Project Structure

The project directory is organized as follows:

* `requirements.txt`: Lists all necessary Python libraries and packages for the project.
* `README.md`: This file, containing project overview and instructions.
* `emotion-fmri-neu/`: Directory containing the 270 `.nii.gz` fMRI data files.
* `workflow.ipynb`: The primary Jupyter Notebook detailing the full project pipeline, allowing for local execution of the entire investigation.
* `report.pdf`: The IEEE-formatted version of the project report, with an abridged analysis.
* `presentation.pdf`: Slide deck offering a project overview and key analysis points.
* `presentation.mov`: A 10-minute recorded presentation of the project.
* `data/`: Directory storing processed `.csv` and `.txt` files.
    * `collinearity/`: Stores `.csv` files showing features after removing those with VIF greater than 5.
    * `cost_function_logs/`: Stores `.txt` logs from dimensionality reduction cost functions.
    * `projections/`: `.csv` files containing data projected from high-dimensional to low-dimensional space.
    * `interpretation/`: `.csv` files aiding in the interpretation of EDA and model training results.
    * `parcellations/`: `.csv` files of data reduced to Region of Interest (ROI) values for each method.
    * `bivariate_data/`: `.csv` files containing two-dimensional embeddings.
    * `models/`: `.pkl` files of trained models for reproducibility.
    * `log_reg_results/`: Outputs from Logistic Regression classification.
        * `classification_reports/`: `.csv` files for evaluation metrics.
        * `coefficients/`: `.csv` files for average coefficient values per feature/method.
        * `errors/`: `.csv` files of all misclassified data instances.
        * `metrics/`: `.csv` of ROC AUC scores.
* `visualizations/`: Directory storing all data visualizations.
    * `atlas_maps/`: Maps visualized at specific coordinates using Nilearn.
    * `collinearity/`: Heatmaps and bar charts evaluating VIF and correlation coefficients.
    * `confusion_matrices/`: Test and train confusion matrices from LogisticRegression().
    * `cost_functions/`: Visualizations demonstrating optimal component numbers for projection methods.
    * `heteroscedasticity/`: Violin plots of heteroskedastic input features.
    * `bivariate_data/`: 2D scatter plots of geometric projection first components, categorized by:
        * `emotion/`: Categorized by emotion class.
        * `subject/`: Categorized by subject ID.
        * `priming/`: Categorized by priming condition.
* `cover-image.png`: Project cover image.
