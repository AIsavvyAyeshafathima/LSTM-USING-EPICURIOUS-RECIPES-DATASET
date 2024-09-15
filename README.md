# LSTM-USING-EPICURIOUS-RECIPES-DATASET
This project uses a Long Short-Term Memory (LSTM) network to generate recipe instructions based on the Epicurious Recipes dataset. The network is trained to predict the next word in a sequence of text, allowing it to generate coherent recipe instructions when given a prompt.

**Table of Contents**
Project Overview
Dataset
Model Architecture
Preprocessing
Text Generation
How to Run
Results
References

**Project Overview**

This project demonstrates how to train an LSTM network on a corpus of recipe data to generate text. The model is designed to predict the next word in a sequence of words, thus generating full recipes based on a given seed text.

The goal of this project is to explore how well LSTM models can learn and generate realistic recipe instructions.

**Dataset**

The dataset used for this project is the Epicurious Recipes dataset, which contains recipes, their ingredients, instructions, and nutritional information.

The dataset can be found on Kaggle:
Epicurious Recipes dataset

**Model Architecture**

The LSTM model consists of the following layers:

1.Embedding layer to convert text into numerical format.

2.Two LSTM layers for learning long-term dependencies.

3.Dense layer with a softmax activation function to predict the next word.

The model is trained using the categorical cross-entropy loss function and the Adam optimizer.

**Preprocessing**

The dataset was cleaned and filtered by concatenating the recipe titles and directions. The text was then tokenized using the Tokenizer from TensorFlow's Keras API. Each recipe was converted into a sequence of words, which was then padded to ensure uniform input lengths.

**Text Generation**

The trained LSTM model generates text by taking a seed phrase (e.g., a recipe title) and predicting the next word in the sequence. This is repeated to generate full recipe instructions. The generated text is influenced by a temperature parameter, which controls the creativity of the output.

Lower temperature values (e.g., 0.5) make the predictions more conservative and repetitive.
Higher temperature values (e.g., 0.8) result in more diverse and creative text.

**Results**

The LSTM network was tested with two different temperature values: 0.5 and 0.8. The following seed prompts were used to generate recipes:

**Temperature: 0.5**

Generated text: recipe for roasted vegetables | chop 1 / 2 cup of vegetables. mix the vegetables with oil and season with salt and pepper . heat the oven to 375 degrees and roast the vegetables for about 30 minutes or until they are tender.

**Temperature: 0.8**

Generated text: recipe for chocolate ice cream | mix in the sugar and egg yolks and whisk until combined . heat the cream and milk in a saucepan over medium heat , stirring constantly until the mixture thickens and coats the back of a spoon . cool and freeze as directed.

**Conclusion**

The LSTM network successfully generates coherent recipe instructions by predicting the next word in a sequence. Lower temperature values (0.5) produce more predictable and straightforward text, while higher temperature values (0.8) generate more diverse and creative responses. The model could be further improved by training on more epochs or tuning hyperparameters.

**References**

Kaggle. (n.d.). Epicurious Recipes dataset. Kaggle. https://www.kaggle.com/datasets/hugodarwood/epicurious-recipes-with-rating-and-nutrition

GitHub. (n.d.). Long Short-Term Memory (LSTM) implementation for text generation. GitHub. https://github.com

Chollet, F. (2015). Keras: Deep Learning for humans. GitHub. https://github.com/keras-team/keras

TensorFlow. (n.d.). Tokenizer API documentation. TensorFlow. https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/text/Tokenizer
