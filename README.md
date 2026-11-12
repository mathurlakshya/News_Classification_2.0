# News Classification 2.0

A machine learning and NLP project that classifies news articles into one of **20 categories** using TF-IDF features and Logistic Regression. The repository also contains an extended notebook exploring transformer-based summarization, named-entity recognition (NER), and question answering.

## Project overview

News articles can cover many different topics. This project builds a text-classification pipeline that learns from labelled news documents and predicts the most likely category for an unseen article or headline.

### Core classification workflow

1. Load the **20 Newsgroups** dataset (by-date train/test split).
2. Explore the training data and distribution of the 20 categories.
3. Convert text into numerical features with **TF-IDF**.
4. Train a **Logistic Regression** classifier.
5. Evaluate predictions using accuracy, a classification report, and a confusion matrix.
6. Try the model on custom text.

## Results

The saved output in the baseline notebook reports **85.33% test accuracy** on 7,532 test documents. This is the result recorded in the notebook; results may vary if the code, data, or configuration changes.

## Repository contents

| File | Description |
|---|---|
| `News_Classification_2_0.ipynb` | Main, reproducible TF-IDF + Logistic Regression classification workflow. |
| `News_Classification_2_0 (1).ipynb` | Extended experiments: the same classifier plus transformer-based summarization, NER, and question-answering demonstrations. |

Start with **`News_Classification_2_0.ipynb`** for the core project. The second notebook is exploratory and may take longer to run because it downloads pretrained transformer models.

## Tech stack

- Python
- pandas
- scikit-learn
- TF-IDF
- Logistic Regression
- Matplotlib and Seaborn
- Hugging Face Transformers (extended notebook)

## Run the project

### Option 1: Google Colab

1. Open the main notebook: [News_Classification_2_0.ipynb](./News_Classification_2_0.ipynb).
2. Select **Open in Colab** (or upload the notebook to Google Colab).
3. Run the cells from top to bottom.
4. When prompted, enter a news headline or short article to see the predicted category.

### Option 2: Run locally

Python 3.10 or newer is recommended.

1. Clone the repository:

   ```bash
   git clone https://github.com/mathurlakshya/News_Classification_2.0.git
   cd News_Classification_2.0
   ```

2. Create and activate a virtual environment:

   **Windows (PowerShell):**
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

   **macOS / Linux:**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open and run `News_Classification_2_0.ipynb` from top to bottom.

The notebook downloads and extracts the 20 Newsgroups by-date dataset when it is not already present. An internet connection is required for the first run.

## Evaluation

The main notebook reports:
- Overall test accuracy
- Precision, recall, and F1-score by category
- Confusion matrix
- Example prediction for custom text

## Notes and limitations

- This is a learning project and a classical text-classification baseline, not a production news-verification system.
- Predictions depend on the categories represented in the training data. The classifier can misclassify short, ambiguous, or out-of-domain text.
- The extended notebook uses pretrained Hugging Face models. Their first run downloads model files and may require substantial memory and time.
- The extended summarization, NER, and question-answering cells are demonstrations, separate from the TF-IDF classifier's evaluation.

## Possible improvements

- Add cross-validation and compare additional classifiers.
- Tune TF-IDF and Logistic Regression hyperparameters systematically.
- Save the trained pipeline and expose it through a small web interface or API.
- Add a clean inference script and automated tests.
- Compare the baseline with transformer-based text-classification models.

## Author

**Lakshya Mathur**

GitHub: [@mathurlakshya](https://github.com/mathurlakshya)

---

This project was created as part of my continued learning in Machine Learning and Natural Language Processing.
