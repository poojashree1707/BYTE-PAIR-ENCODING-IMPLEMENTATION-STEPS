## Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch

## Project Overview

This project implements a Custom Byte Pair Encoding (BPE) Tokenizer from scratch using Python and a simple Next Word Prediction model. The BPE tokenizer learns subword vocabulary by repeatedly merging the most frequent adjacent character pairs, while the prediction model suggests the next word based on previously seen word sequences.

#### The project demonstrates fundamental Natural Language Processing (NLP) concepts without relying on external machine learning libraries.
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
- Encodes new words using learned merge rules.
- Decodes encoded tokens back into original words.
- Displays vocabulary statistics using NumPy.

## Next Word Prediction

- Builds a simple language model from a text corpus.
- Stores relationships between consecutive words.
- Predicts the most likely next word.
- Interactive command-line prediction.
- Simple and lightweight implementation.

## Project Structure

├── corpus.txt  

├── bpe_tokenizer.py 

├── next_word_prediction.py 

└── README.md

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

## Example Next Word Prediction
## Input
### Enter text:
### i love
## Output
### Next Word: you

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

### Conclusion

#### This project successfully implements a Byte Pair Encoding (BPE) Tokenizer and a Next Word Prediction model using Python. The BPE tokenizer learns subword vocabulary through frequent pair merging, while the prediction model suggests the most likely next word based on the training corpus. Together, they demonstrate the basic concepts of Natural Language Processing (NLP) and provide a foundation for building more advanced language models.


