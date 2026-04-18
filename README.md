# Theoretical Foundations of Large Language Models: Text Prediction and Limitations

The thesis focuses on the theoretical principles that make Large Language Models able to generate text. Its central idea is that LLMs should be understood as deep learning systems trained to predict the next token in a sequence, rather than as systems that store explicit knowledge or understand language in the human sense. From this starting point, the work explains the mathematical and architectural foundations behind text generation and then discusses the main limitations that follow from those foundations.

This work was developed during the 2025–2026 academic year at Università degli studi di Milano-Bicocca

## Main Topics Covered

-Neural Networks and Deep Learning: LLMs are fundamentally very large deep learning models. Concepts such as parameters, loss functions, backpropagation, and gradient descent also apply to LLMs.

-How large language models are trained, including tokenization, next-token prediction, softmax, cross-entropy loss, parallel computation & mini-batch training, and AdamW optimizer. This part explains how LLMs acquire the ability to produce fluent text by learning statistical regularities from large amounts of data.

-Embeddings, which represents tokens as vectors in a high-dimensional numerical space. LLMs do not operate directly on words, but on their numerical representations, and those representations are the basis for all later computations in the model.

-Transformer architecture used in modern LLMs, introduced as a response to the limitations of RNNs, and explained through its core components, including positional encoding, attention mechanisms, decoder blocks, output probability computation, and decoding strategies such as argmax and top-p sampling

-Main limitations of large language models, such as hallucinations, the grounding problem, context window constraints, controllability and computational cost.
