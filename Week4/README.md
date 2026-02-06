# Lab 4: Introduction to Generative AI - Text Generation

## 1. Objective
[cite_start]The objective of this lab is to design and implement simple text generation models that can learn patterns from a specific text corpus and generate new, meaningful text sequences[cite: 3, 4]. The lab explores three different approaches to this task, ranging from statistical methods to deep neural networks.

## 2. Dataset
[cite_start]The project uses a small, domain-specific text corpus related to **Artificial Intelligence and Modern Technology**[cite: 30].
- **Content:** Sentences covering topics like machine learning, neural networks, ethics in AI, and education technology.
- [cite_start]**Preprocessing:** The raw text is cleaned (converted to lowercase, stripped of whitespace) and tokenized before being fed into the models[cite: 23].

---

## 3. Workflow & Components

### Part A: N-Gram Baseline (Statistical Approach)
Before implementing neural networks, a statistical N-Gram model is used as a baseline.
- [cite_start]**Implementation:** A custom `SimpleNGram` class[cite: 15].
- **Logic:** It builds a probability chain where the next word is predicted based on the previous $N-1$ words.
- **Key Function:** `fit()` to build the chain and `predict()` to generate text.

### Part B: Component-I - RNN/LSTM Model
[cite_start]This component implements a Recurrent Neural Network using Long Short-Term Memory (LSTM) units to handle sequential data[cite: 20, 25].

1.  **Preprocessing:**
    * Tokenizer converts words to integers.
    * Input sequences are created using a sliding window approach.
    * [cite_start]Sequences are padded to ensure uniform length[cite: 23].
2.  **Architecture (`lstm_net`):**
    * **Embedding Layer:** Converts integer tokens into dense vectors.
    * **LSTM Layer:** Captures temporal dependencies in the text (100 units).
    * **Dense Layer:** Uses Softmax activation to output probabilities for the next word.
3.  **Training:** The model is trained for 100 epochs using `categorical_crossentropy` loss.

### Part C: Component-II - Transformer Model
[cite_start]This component implements a modern Transformer-based architecture using Self-Attention mechanisms[cite: 46, 74].

1.  **Custom Layers:**
    * [cite_start]`PositionalEmbedding`: Adds information about the position of words to the embeddings, as Transformers process data in parallel[cite: 78].
    * [cite_start]`EncoderLayer`: Implements Multi-Head Attention and Feed-Forward networks with normalization and dropout[cite: 79].
2.  **Architecture (`trans_model`):**
    * Input -> Positional Embedding -> Transformer Encoder Block -> Global Average Pooling -> Dense Layers -> Output.
3.  [cite_start]**Training:** The model is trained for 150 epochs to ensure convergence on the small dataset[cite: 80].

---

## 4. How to Run
1.  **Setup:** Run the first cell to load libraries and clean the dataset.
2.  **N-Gram:** Run the second cell to see baseline text generation results.
3.  **LSTM:** Run the Component-I cell to train the LSTM network and view the generated text outputs.
4.  **Transformer:** Run the Component-II cell to train the Transformer network and compare the results with the LSTM output.
