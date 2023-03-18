# Finetune layoutLM model

In this notebook, we are going to fine-tune LayoutLMv2ForSequenceClassification on the RVL-CDIP dataset, which is a document image classification task. Each scanned document in the dataset belongs to one of 16 classes, such as "resume" or "invoice" (so it's a multiclass classification problem). The entire dataset consists of no less than 400,000 (!) scanned documents.

For demonstration purposes, we are going to fine-tune the model on a really small subset (one example per class), and verify whether the model is able to overfit them. Note that LayoutLM achieves state-of-the-art results on RVL-CDIP, with a classification accuracy of 94.42% on the test set.

Original LayoutLMv2 paper: https://arxiv.org/abs/2012.14740
