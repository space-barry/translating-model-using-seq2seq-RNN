# Language Translation Model

This project implements an English-to-Spanish **language translation model** using **neural machine translation** with a **seq2seq architecture**.

## Overview

We use an **Encoder-Decoder LSTM model** with a **seq2seq architecture** to tackle this many-to-many sequence problem. This approach is commonly used for various tasks including text summarization, chatbot development, and neural machine translation.

## Dependencies

- Tensorflow
- Keras
- Numpy
- Graphviz

Install dependencies:
```
pip install -r requirements.txt
brew install graphviz
```

## Dataset

We use the English-Spanish corpus from [Tatoeba Project](http://www.manythings.org/anki/). Download `spa-eng.zip` and save it in `data/spa-eng/spa.txt`.

## Model Architecture

Our Neural Machine Translation model consists of two LSTM layers:
- **Encoder LSTM**: Processes the input sentence in English
- **Decoder LSTM**: Generates the output sentence in Spanish

## Preprocessing and Tokenization

1. Tokenize input and output sentences
2. Convert words to integers
3. Create word-to-index dictionaries
4. Pad sentences to uniform length

## Word Embeddings

We use pre-trained [GloVe](https://nlp.stanford.edu/projects/glove/) word embeddings from Stanford CoreNLP project.

## Model Creation and Training

1. Create embedding layer
2. Define encoder and decoder LSTMs
3. Define final output layer (Dense)
4. Train the model

## Prediction Model

We modify the trained model for making predictions:
1. Use encoder to process input sentence
2. Use decoder to generate output words one by one
3. Continue until end-of-sentence token is encountered

## Making Predictions

1. Convert input sentence to integer sequence
2. Pass through encoder to get hidden and cell states
3. Use decoder to predict words sequentially
4. Convert predicted integers back to words

## Testing and Improvements

- Randomly select sentences for translation
- Increase number of epochs for better results (default is 5)
- Use more training data to reduce overfitting

## Conclusion

This project demonstrates the use of seq2seq architecture for neural machine translation. While effective at mapping input-output relations, it has limitations in capturing context for more advanced applications like chatbots.

## Future Work

- Implement attention mechanism for better context handling
- Experiment with transformer architecture
- Expand to multi-language translation

Feel free to contribute or reach out with any questions!



Medium link  https://medium.com/@khanmuhammadaizazullah/bridging-translating-languages-our-journey-into-neural-machine-translation-%EF%B8%8F-21fffbf89b02 
