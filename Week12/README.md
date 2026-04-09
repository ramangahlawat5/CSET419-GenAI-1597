# Lab 12 – Generative Model with Attention

## Objective
Implement a text generation model using attention to improve contextual understanding.

## Workflow
1. **Preprocessing**: 
   - Load the Cornell Movie Dialog dataset.
   - Clean the text by lowercasing and removing special characters.
   - Tokenize the data and build a vocabulary mapping words to unique integer indices.
2. **Model Design**: 
   - **Embedding Layer**: Map input tokens into dense vectors.
   - **LSTM Encoder**: Process input sequences to capture long-term dependencies.
   - **Attention Mechanism**: Implement Bahdanau (additive) attention to calculate weights for each input word.
   - **Output Layer**: Map the combined context and hidden states to the vocabulary size to predict the next word.
3. **Training**: 
   - Train the model using `CrossEntropyLoss` (ensuring the padding index is ignored).
   - Optimize parameters using the **Adam optimizer**.
4. **Evaluation**: 
   - Check generated responses from the chatbot to ensure contextual relevance.
   - Visualize the attention weights (heatmaps) to observe which input words the model focuses on during text generation.

## Output
- A functional interactive chatbot capable of generating replies from user input.
- Visual attention maps demonstrating that the model focuses on specific relevant tokens (e.g., highlighting focus on the word "you" when responding to "how are you").
