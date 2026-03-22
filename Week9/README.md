# Lab 9 – Sequence Generation

## Objective
The objective of this lab is to understand how generative models can be applied to sequential data such as text, time-series, or language sequences. Students will design and implement simple generative models capable of learning patterns from sequences and generating new sequences.

## Learning Outcomes
After completing this lab, students will be able to:
* Understand sequential data and its characteristics.
* Learn how generative models work for sequence prediction.
* Implement sequence-based generative models using neural networks.
* Train models to generate new sequences from learned patterns.
* Evaluate the quality of generated sequences.

---

## Workflow

### Component I: Sequence Generation using RNN / LSTM

1. **Data Preprocessing**: Load the sequential dataset and convert sequences into numerical representations (tokenization).
2. **Sequence Pairing**: Create input-output sequence pairs using a sliding window or N-gram approach.
3. **Model Design**: Implement an RNN or LSTM-based architecture with an Embedding layer and a Dense output layer.
4. **Training**: Train the model on the prepared sequence dataset.
5. **Generation**: Use a seed input to generate new sequences by predicting the next element iteratively.

### Component II: Transformer Based Sequence Generation

1. **Tokenization**: Use the same dataset and perform word-level or subword tokenization.
2. **Positional Encoding**: Implement positional encoding to provide the model with information regarding the order of the sequence.
3. **Model Design**: Design a Transformer-based architecture incorporating Multi-Head Attention and Feed-Forward networks.
4. **Training**: Train the Transformer model on the sequence dataset.
5. **Generation**: Generate text samples and compare the results with the LSTM model.

---

## Expected Output
* **Generated Sequence Samples**: New text sequences produced by the LSTM model.
* **Transformer Outputs**: High-quality generated sequences from the Transformer architecture.
* **Evaluation**: A comparison of the loss and generation quality between the two models.
