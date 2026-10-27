# Multihead-Context_Aware-RoBERTa-for-Dialogue-Act-Classification
A notebook detailing my submission for the Machine Learning for Language and Vision module for my MSc in Artificial Intelligence @ UWE

## Task Overview
The dataset - [Daily Dialog](https://arxiv.org/abs/1710.03957) -  assigned to this fairly open-ended task contains minimally pre-processed dialogues as strings. The lecturer added further errors in order to test pre-processing skills, and the students were asked to create an NLP solution of their choice. As such, I interpreted this as a **multiclass dialogue act classification problem**.

## Method
Further analysis revealed two suitable classes for classification: `Topic` and `Dialogue_Act` (DA); the latter class's labels denote the type of utterance in a dialogue section, i.e., questions and directives. Thus, a system was designed that could classify both classes, while using the context of preceding utterances to aid classification of the current utterance being classified. [RoBERTa](https://huggingface.co/docs/transformers/en/model_doc/roberta) was chosen as the base model based on its performance in similar tasks and re-tuned with two classification heads. **Multihead Context-Aware RoBERTa for Dialogue Act Classification**

## Evaluation 
An overall accuracy of **83.5%** was recorded for DA classification, while Topic classification was 52.2%. 

Macro F1 for DA was **78.1%**, while for Topic it was 36.1%. Looking at F1 scores for individual labels within the more successful DA classification reveals that `Question` receives **92.5%** and `Inform` **87.2%**. 
