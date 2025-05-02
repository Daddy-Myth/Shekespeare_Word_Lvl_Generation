# Shakespeare Word-Level Language Model

This project implements a word-level language model trained on the works of William Shakespeare. The model is built using PyTorch and learns to generate Shakespearean-style text by predicting the next word in a sequence.

## Overview

This notebook demonstrates:

- Preprocessing of Shakespeare’s text at the word level
- Vocabulary construction and tokenization
- Model definition using an embedding layer, GRU, and a linear output layer
- Training loop with loss tracking
- Generation of Shakespearean-like text given a seed phrase

## Features

- Word-level text processing
- Custom vocabulary class to map words to indices and back
- GRU-based language model
- Text generation with temperature sampling
- Easy-to-follow code structure for educational purposes

## Model Architecture

- **Embedding Layer**: Transforms word indices into dense vectors
- **GRU**: Captures temporal dependencies in word sequences
- **Linear Layer**: Maps GRU outputs to vocabulary logits

## Project Structure

```
Shekespeare_Word_Lvl.ipynb       # Jupyter Notebook with full implementation
data/
└── shakespeare.txt              # Text file containing Shakespeare’s works
```

## Requirements

- Python 3.7+
- PyTorch
- NumPy
- Matplotlib
- tqdm

Install dependencies with:

```bash
pip install torch numpy matplotlib tqdm
```

## Training

The model is trained using negative log-likelihood loss. The training loop includes:

- Mini-batch processing
- Randomized start points for sequences
- Logging of loss values over time

## Text Generation

After training, you can generate text by providing a starting prompt:

```python
generate(model, "To be or not to be", max_new_tokens=50)
```

Adjust the temperature parameter to control randomness in the output.

## Sample Output

```
To be or not to be I know not whence to go
But though the soul be fled from death's own blow
```
