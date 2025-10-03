
Before training a **LLM**, we need to process the dataset so it can be used effectively. Since deep learning models **cannot directly interpret raw text**, we must transform words into numerical representations.

This transformation is done through **embeddings**, which convert words into continuous-valued vectors. Embeddings are essential for neural networks because they allow non-numeric data — such as text, images, and audio — to be represented in a way that models can process. However, different types of data require distinct embedding techniques. For example, an embedding method tailored for text cannot be used interchangeably with audio or video.

The **main role of embeddings** is to turn unstructured text into structured numerical data that machine learning models can understand. LLMs typically generate and refine their own embeddings during training. For example, smaller versions of **GPT-2 (with 117M to 125M parameters)** use a **768-dimensional embedding space** to represent words effectively.

## Tokenization: Converting Text into Processable Units

Training an LLM involves breaking down text into smaller components. The process includes:

- **Splitting sentences into words**
- **Converting words into tokens**
- **Mapping tokens to embeddings**

However, a key challenge in tokenization is dealing with **unknown words** ; words that were not included in the training data. To manage this, special tokens are added to the vocabulary:

- <|unk|> represents words that are not part of the model’s predefined vocabulary.
- <|endoftext|> serves as a separator for distinct pieces of text.

These tokens act as **markers**, helping the model understand when a text segment begins or ends.

## Byte Pair Encoding (BPE)

GPT models use **Byte Pair Encoding (BPE)**, a more advanced tokenization technique that improves how models handle unfamiliar words. Unlike traditional methods that replace unknown words with <|unk|>, BPE **decomposes them into smaller subword units or even individual characters**.

For instance, if a word is not found in the vocabulary, BPE doesn’t discard it. Instead, it breaks it down into its **most common subcomponents**, allowing the model to process it without needing a special unknown token.

BPE builds its vocabulary progressively:

1. **Initially, it treats each character as an individual token** (ex: “a,” “b,” “c”).
2. **It then merges frequently co-occurring character pairs** into subwords (ex: “d” and “e” might combine into “de”).
3. **This process continues until a predefined vocabulary size is reached**.

Because of this approach, **LLMs trained with BPE can handle words they have never seen before**, ensuring they remain effective across various types of text.

## Understanding Embeddings in LLMs

Since LLMs process text as tokenized sequences, each token needs to be mapped to a corresponding **embedding vector**. This mapping occurs through a **weight matrix**, where:

- **Rows represent tokens from the vocabulary**.
- **Columns represent different embedding dimensions**.

For example, if an embedding matrix has **four** **rows and three columns**, each row corresponds to a token, while each column represents a numerical feature of the embedding.

## Positional Information

In addition to token embeddings, LLMs also need **positional encodings** to capture the order of words in a sequence. There are two primary approaches:

1. **Absolute Positional Embeddings**: Each word receives a **unique position-based encoding** that directly represents its place in the sequence. OpenAI’s GPT models use this technique.
2. **Relative Positional Embeddings**: Instead of marking the exact position of a word, this approach encodes the **relative distance between words**. This method helps the model generalize better to sequences of varying lengths, even if it hasn’t encountered those specific lengths during training.

By incorporating **positional embeddings**, LLMs can better **understand sentence structure and contextual relationships between words**, improving their ability to generate meaningful responses.

![[Pasted image 20251003150431.png]]
