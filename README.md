```markdown
# Shakespeare Character-Wise Language Model

This project implements a character-level language model trained on the works of William Shakespeare. Built using PyTorch, the model learns to generate Shakespearean-style text one character at a time, capturing the rhythm and structure of classical literature.

## Overview

This notebook demonstrates:

- Character-level preprocessing of Shakespeare’s text  
- Vocabulary construction and one-hot encoding  
- A simple neural network using embeddings and GRU layers  
- Training the model using cross-entropy loss  
- Generation of character sequences using temperature sampling

## Features

- Character-level modeling for finer control over language style  
- Custom vocabulary class to map characters to indices and back  
- GRU-based recurrent neural network  
- Temperature-controlled text generation  
- Lightweight and educational implementation

## Model Architecture

- **Embedding Layer**: Translates character indices into dense vector representations  
- **GRU Layer**: Processes sequential character inputs and captures dependencies  
- **Linear Layer**: Projects GRU output to character logits for prediction

## Project Structure

```
Another_Shakespeare_char_Wise.ipynb   # Jupyter Notebook with full implementation  
data/  
└── shakespeare.txt                   # Text file with Shakespeare's works  
```

## Requirements

- Python 3.7+  
- PyTorch  
- NumPy  
- tqdm  

Install dependencies with:

```bash
pip install torch numpy tqdm
```

## Training

The model is trained using cross-entropy loss. The training loop includes:

- Random sequence extraction from the dataset  
- Batched training with sequence windows  
- Periodic loss tracking for monitoring

## Text Generation

After training, generate Shakespearean text by providing a seed string:

```python
generate(model, "To thine own self be", max_new_tokens=100)
```

The `temperature` parameter can be adjusted to control creativity and randomness.

## Sample Output

```
To thine own self be true,
And it must follow, as the night the day,
Thou canst not then be false to any man.
```
```
