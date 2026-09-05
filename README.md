# BERT with FHE

This project explores privacy-preserving text classification by combining BERT sentence representations with a classifier that supports Fully Homomorphic Encryption (FHE). It was developed collaboratively as a course project.

The experiment uses the 20 Newsgroups dataset. Text documents are first converted into 768-dimensional embeddings with `bert-base-cased`. A logistic regression classifier from Concrete ML is then trained on the embeddings, compiled for FHE, and evaluated using both clear and encrypted inference.

> FHE is applied to the classifier inference stage in this implementation. BERT embedding generation is performed separately in clear text.

## Workflow

1. Load and preprocess the 20 Newsgroups dataset.
2. Generate document embeddings with a pretrained BERT model.
3. Train a logistic regression classifier using Concrete ML.
4. Compile the classifier for FHE execution.
5. Compare predictions from clear and encrypted inference.

## Repository contents

- [`bert_with_fhe_20newsgroups.ipynb`](bert_with_fhe_20newsgroups.ipynb): the original Colab-based experiment, with execution outputs removed.
- [`The Implementation of BERT over FHE.pdf`](The%20Implementation%20of%20BERT%20over%20FHE.pdf): the complete project report, including the methodology and experimental results.

## Running the notebook

The notebook was designed for Google Colab and installs its required packages in the setup cells. Run the cells in order in a Colab runtime. Generating BERT embeddings and compiling the FHE model may take considerable time depending on the available hardware.

The notebook reflects the package ecosystem used when the project was completed in 2023. Current releases of its dependencies may require compatibility adjustments.
