# Minimize the unintended bias in toxicity classification
This is a NLP course project of DATA130030.01(2024 Spring) in Fudan University, professored by Baojian Zhou.

We design a framework to minimize the unintended bias in toxicity classification problems. This project is based on the Kaggle competition [Jigsaw: Unintended Bias in Toxicity Classification](https://www.kaggle.com/competitions/jigsaw-unintended-bias-in-toxicity-classification/). The dataset provided allow us to use auxiliary labels(all binary) to better the toxicity classification results(i.e. reducing the unintended bias). Instead of seeking for high **accuracy**, we focus more on **Recall**, which is more aligned with the competition goal.

Our method is comprised of a **auxiliary BERT tagger** (complement the auxiliary labels, many of which are missing in the original dataset) and **a LoRA fine-tuned BERT** for multi-task learning with all the auxiliary labels. By ensembled with a multi-task learning LSTM, we achieved 89.89\% Recall on test dataset.
