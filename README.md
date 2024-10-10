# Spelling Correction Tool Using NLP

This project is a simple spelling correction tool built using Natural Language Processing (NLP) techniques in Python. It detects and corrects misspelled words by leveraging a large text corpus for word frequency analysis combined with an edit-distance algorithm to find the most probable corrections.

## Features

- Automatically detects misspelled words in a sentence.
- Corrects words based on a probabilistic model using word frequencies from a large corpus.
- Uses edit distance (insertions, deletions, transpositions, and replacements) to generate correction candidates.
- Handles both single and multi-word input sentences.

## How It Works

1. **Corpus-Based Word Frequency Model**: The tool loads a large text corpus to calculate word frequencies. This helps determine which words are more likely correct based on their frequency in the corpus.
2. **Edit-Distance Algorithm**: For each misspelled word, the tool generates possible corrections by creating variations of the word through common spelling errors (edits). These edits include:
   - Insertion
   - Deletion
   - Replacement
   - Transposition
3. **Candidate Selection**: The most probable correction is selected from the generated candidates based on its frequency in the corpus.

## Installation

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Conda (optional but recommended)

### Install Required Libraries

If you're using Conda, install the following dependencies:

```bash
conda install numpy
conda install -c conda-forge nltk
```

Or install them via pip:

```bash
pip install numpy
pip install nltk
```

### Downloading a Corpus

You can use a larger corpus like the Gutenberg dataset from the `nltk` library. To download the dataset:

```python
import nltk
nltk.download('gutenberg')
```

## Usage

1. Clone the repository and navigate to the project folder.
2. Run the Jupyter notebook to load the tool.
3. In the notebook, you can input any sentence with misspellings, and the tool will output the corrected sentence.

### Example

Input sentence with misspellings:

```text
Ths is an exampel of a sentnce with sevral mispelled wrds.
```

Corrected sentence:

```text
This is an example of a sentence with several misspelled words.
```
