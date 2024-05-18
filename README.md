
# Impact of Data Bias on AI Models

## Overview
This project investigates the effect of data bias on the performance of AI models, specifically focusing on how variations in the composition of emotional data affect learning outcomes. The research was presented at the Spring Conference of the Korean Society for Human Engineering, held on May 19, 2023, by Inheon Choi and Sangwon Lee from the Department of Industrial and Management Engineering at Korea University.

## Table of Contents
1. [Introduction](#introduction)
2. [Methodology](#methodology)
3. [Result Analysis](#result-analysis)
4. [Conclusion](#conclusion)

## Introduction
The field of artificial intelligence has evolved from simple perceptrons and neural networks to sophisticated models like CNNs for image processing and RNNs for natural language processing. Recently, generative AI models such as ChatGPT and Copilot have been developed, focusing on human-emotional AI interactions.

Previous research has extensively studied human reactions to emotional AI and the communication between humans and AI with emotions. However, there is a limitation in experimental research on how AI models change based on emotional criteria.

## Objective
This study aims to analyze the relationship between the changes in the composition of emotional data and the outcomes produced by AI models. By quantitatively analyzing the effects of varying emotional composition ratios, we seek to understand how these changes influence the models.

## Methodology
![image](https://github.com/ih9511/sentiment-analysis-for-biased-data/assets/46120405/66473868-bf11-4afa-b3de-00959cfb0312)
### Imbalanced Dataset
To understand the impact of data imbalance, we examined the issue of imbalanced datasets in AI. Data imbalance can lead to overfitting and decreased accuracy. Various methods such as oversampling, undersampling, and weighted learning have been researched to handle imbalanced datasets.

### Data Selection
We used two datasets: MS-COCO and SentiCap. MS-COCO contains over 320,000 images with 2.5 million labeled instances, while SentiCap is based on MS-COCO and includes captions with emotional content. The data was restructured into subsets with different ratios of positive to negative captions: 80:20 (P8N2), 60:40 (P6N4), 40:60 (P4N6), and 20:80 (P2N8).

### Model Structure
We employed a CNN-RNN based image captioning model. The CNN acts as an encoder to extract features from images, and the RNN acts as a decoder to generate sequences of words (captions). The model was trained on datasets with varying emotional compositions.

## Result Analysis
The models' generated captions were analyzed using the Sentiment Intensity Analyzer (SIA) from the NLTK library. The analysis showed that as the ratio of positive to negative captions decreased, the models generated more positive captions.

### SIA Results
- **Positive Average:** Decreased as the ratio of positive captions decreased.
- **Negative Average:** Increased as the ratio of positive captions decreased.
- **Neutral Average:** Varied across models but generally increased as the ratio of positive captions decreased.

## Conclusion
The study revealed that the degree of data imbalance significantly affects the AI model's outputs. Specifically, a higher proportion of positive data leads to the generation of more positive captions, even when negative data is introduced. This insight is crucial for developing more balanced and human-like AI interactions, emphasizing the importance of emotional data composition in training AI models.
