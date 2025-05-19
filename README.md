# WordBaz-NLP 

WordBaz-NLP is a project focused on creating, evaluating, and comparing Persian word embeddings. It involves training a custom Word2Vec model on the Persian "SLPL/naab" corpus and comparing its performance against pre-trained FastText embeddings (`cc.fa.300.vec`).

## Key Features & Steps:

1.  **Data Handling:** Loading and sampling the "SLPL/naab" corpus using the `datasets` library.
2.  **Text Preprocessing:** Standard Persian text preprocessing (normalization, non-Persian character removal, tokenization, stopword/short token removal) using the `hazm` library.
3.  **Word2Vec Training:** Training a custom Word2Vec model (Skip-gram, 100 dimensions) on the preprocessed Naab data using `gensim`.
4.  **Word2Vec Evaluation & Visualization:**
    *   Assessing semantic similarity (e.g., for the word "دانشگاه" - university).
    *   Visualizing the top 100 word embeddings using PCA with `scikit-learn` and `matplotlib`.
5.  **FastText Pre-trained Model:**
    *   Downloading and loading pre-trained Persian FastText embeddings.
    *   Evaluating semantic similarity using FastText.
6.  **Comparative Analysis:** Comparing the semantic similarity results from the custom Word2Vec model and the pre-trained FastText model on a set of test words (e.g., "کتاب", "دانشگاه", "سلامت", "ایران", "زن", "علم").

##  Key Findings:

*   The custom **Word2Vec (Naab)** model demonstrates strong contextual understanding for in-corpus vocabulary and morphological consistency.
*   The pre-trained **FastText (cc.fa)** model, trained on a much larger corpus, shows greater robustness in handling word variants, misspellings, and out-of-vocabulary (OOV) words due to its subword information.
*   The choice between models depends on the use case: precision within a focused corpus (Word2Vec) versus generalization across diverse inputs (FastText).

##  Technologies Used:

*   Python
*   `datasets`
*   `hazm`
*   `gensim`
*   `matplotlib`
*   `scikit-learn (sklearn)`
*   Jupyter Notebook

---
*This project explores different approaches to Persian word embeddings.*