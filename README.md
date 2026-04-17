# Theoretical Foundations of Large Language Models: Text Prediction and Limitations

The thesis focuses on the theoretical principles that make Large Language Models able to generate text. Its central idea is that LLMs should be understood as deep learning systems trained to predict the next token in a sequence, rather than as systems that store explicit knowledge or understand language in the human sense. From this starting point, the work explains the mathematical and architectural foundations behind text generation and then discusses the main limitations that follow from those foundations.

This work was developed during the 2025–2026 academic year at Università degli studi di Milano-Bicocca

## Thesis Structure

### 1. Introduction

This chapter explains that an LLM generates text autoregressively: a prompt is tokenized, the model estimates a probability distribution over the vocabulary for the next token, one token is selected, and the process repeats until generation ends.

By presenting LLMs as probabilistic deep learning models rather than systems with unlimited knowledge, it introduces the concepts needed for the later chapters. The distinction between apparent intelligence and statistical next-token prediction is essential to understanding both the strengths and limitations of LLMs.

### 2. Neural Networks

This chapter introduces the fundamental learning principles underlying LLMs. It begins with the perceptron and its limitation to linear decision boundaries, activation functions, multi-layer perceptrons, feedforward computation, loss functions, backpropagation, and gradient descent.

Large language models are deep neural networks with vast numbers of parameters, and their behavior is determined by the same principles of neural network training described above. Parameters determine predictions, loss functions quantify error, gradients indicate how parameters should be updated, and iterative optimization reduces that error over time. Understanding these foundations allows the later discussion of LLM training to be interpreted meaningfully.

### 3. Training Large Language Models

The third chapter uses GPT-3 as an example to show how parameters are distributed across embeddings, attention layers, feedforward layers, and the output projection. It also describes the composition of training data, tokenization, pre-training through next-token prediction, mini-batch training, softmax, cross-entropy loss, gradients with respect to logits, mini-batch stochastic gradient descent, and the AdamW optimizer.

This chapter is central to the thesis because it describes how LLMs acquire their ability to generate coherent language. It shows that the model is not trained to verify truth directly, but to assign higher probability to tokens that fit the context according to patterns learned from large corpora. The discussion of fine-tuning and alignment also clarifies why a pre-trained language model is not automatically a helpful assistant.

### 4. Embeddings

The embeddings chapter explains how language is converted into numerical form. Since machines cannot process words directly, tokens are represented as vectors in high-dimensional spaces. The chapter defines embeddings, discusses semantic similarity through cosine similarity and dot product, introduces static embeddings such as Word2Vec, and describes how some semantic relationships can appear as vector relationships. It also examines the limitations of static embeddings when a word has multiple meanings, before introducing contextual embeddings.

Embeddings are closely tied to LLMs because every token processed by a language model begins as a vector representation. The thesis shows that these vectors are not arbitrary labels: their geometry can reflect semantic similarity and relationships between words. This is important for understanding LLMs because transformer layers operate by transforming these token vectors into contextual representations. Without embeddings, there would be no numerical structure on which attention, feedforward layers, or output prediction could operate.

### 5. Transformers

The transformers chapter examines the architecture used by modern LLMs. It begins with recurrent neural networks, explaining how they process sequences one token at a time and why this leads to limitations such as inefficient sequential computation, vanishing gradients, degradation of long-range dependencies, and limited context capacity. These limitations motivate the introduction of the transformer architecture, designed to overcome them, with particular focus on the decoder-only structure used in many modern language models.

The chapter explains positional encoding, self-attention, multi-head attention, masked self-attention, feedforward networks, residual connections, layer normalization, stacked decoder blocks, and the output layer. It also discusses how logits are converted into probabilities and how generation can use strategies such as argmax selection, top-p sampling, and temperature.

### 6. Limitations of Large Language Models

 It discusses the grounding problem, hallucinations, context window length, controllability and computational cost. The model learns from text rather than from direct experience of the physical world, so it may produce answers that are linguistically plausible while missing practical constraints. It may also generate fluent but false statements because its objective is based on probable token continuation, not truth verification.
