## Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch

## Project Overview

This project implements the **Byte-Pair Encoding (BPE)** algorithm from scratch using **Python** and **NumPy**. BPE is a subword tokenization technique widely used in modern Natural Language Processing (NLP) models such as GPT, BERT, and RoBERTa. The tokenizer learns frequently occurring character pairs and merges them iteratively to create subword tokens.

---

## Objective

The objective of this project is to:

- Understand the working of the Byte-Pair Encoding algorithm.
- Learn how subword vocabularies are created.
- Implement BPE without using external NLP libraries.
- Encode and decode words using learned merge rules.
- Analyze the generated vocabulary using NumPy.

---

## Features

- Reads text corpus from a file.
- Preprocesses text by converting it to lowercase.
- Builds initial character-level vocabulary.
- Finds the most frequent adjacent symbol pairs.
- Learns merge rules iteratively.
- Generates subword vocabulary.
- Encodes new words using learned merge rules.
- Decodes encoded tokens back into original words.
- Displays vocabulary statistics using NumPy.

---

## Project Structure

```
BPE-Tokenizer/
│
├── corpus.txt
├── bpe_tokenizer.py
└── README.md
```

---

## Corpus Used

Example corpus:

```
low
lower
lowest
new
newer
widest
```

Each word is treated as a sequence of characters followed by the special end-of-word token:

```
l o w </w>
l o w e r </w>
```

---

## Algorithm Workflow

1. Read the corpus.
2. Preprocess the text.
3. Build initial vocabulary.
4. Count adjacent character pairs.
5. Find the most frequent pair.
6. Merge the pair into a new token.
7. Repeat for a fixed number of merges.
8. Build the final vocabulary.
9. Encode new words.
10. Decode tokens back to words.
11. Display vocabulary statistics.

---

## Sample Output

### Learned Merge Rules

```
1. ('l', 'o')
2. ('lo', 'w')
3. ('low', 'e')
4. ('r', '</w>')
5. ('s', 't')
6. ('st', '</w>')
7. ('n', 'e')
8. ('ne', 'w')
9. ('low', '</w>')
10. ('lowe', 'r</w>')
```
## Applications

- Natural Language Processing
- Machine Translation
- Text Generation
- Chatbots
- Speech Recognition
- Large Language Models (LLMs)

---

## Future Enhancements

- Train on larger datasets.
- Allow user-defined number of merge operations.
- Save and load learned vocabularies.
- Visualize merge frequencies.
- Compare with WordPiece and SentencePiece tokenizers.

---

## Conclusion

This project demonstrates how Byte-Pair Encoding (BPE) builds a subword vocabulary by repeatedly merging the most frequent adjacent character pairs. The implementation provides a clear understanding of tokenization, vocabulary construction, encoding, and decoding, making it an excellent educational project for learning the fundamentals of NLP tokenization techniques.

---

