# Text Detoxification with Large Language Models

## Overview
This project explores advanced strategies using Large Language Models (LLMs) for detoxifying harmful digital content without the need for simple deletion. Utilizing the latest innovations in Natural Language Processing (NLP), our work leverages models such as DiffuDetox, Attribute-Discriminative Language Model (ADLM), and rectification techniques. These methods are designed to mitigate toxicity while preserving the linguistic fluency and integrity of the content.

## Key Features
- **Advanced Detoxification Techniques:** Integration of cutting-edge models like DiffuDetox and ADLM that ensure non-toxic output while maintaining content quality.
- **Comprehensive Evaluation Metrics:** Utilizes Style Transfer Accuracy (STA), content preservation (SIM), and character n-gram F-score (ChrF) to evaluate the performance.
- **Innovative Dataset Use:** Implementation of parallel datasets developed by Logacheva et al. for effective training and testing.

| Language | Toxic sentence                             | Neutral sentence                      |
|----------|--------------------------------------------|---------------------------------------|
| en       | sh*t just got real upload.                | Things just got real upload.         |
| de       | Nö, der sieht d*mm aus.                   | Nö, der gefällt mir optisch nicht.   |

## Experimentation
We employed several experimental approaches:
- **Fine-tuning mT5:** Leveraged for its multilingual capabilities across various NLP tasks.
- **Few-shot prompting with flan-T5-XL and mGPT:** Explored to understand the efficacy of LLMs in a few-shot setup.
- **Contextual Prompt Adjustment (CoPA):** A novel approach for improving selection among detoxified outputs.

| dataset | J-score |
|---------|---------|
| dev     | 0.362   |
| test    | 0.316   |


## Challenges and Innovations
- **Multilingual Support:** Addressing the challenge of language variety in toxic content across different datasets.
- **Preservation of Original Meaning:** Ensuring that the detoxification process does not alter the original intent of the content.
- **Meta-Learning Techniques:** Experimenting with meta-learning setups like CoPA for enhanced prediction accuracy.

## Conclusion
This project signifies a step forward in the safe and responsible management of user-generated content on digital platforms. By harnessing the power of LLMs and innovative NLP techniques, it is possible to create a healthier online environment without compromising on content quality or freedom of expression.

## Future Work
- **Expand Language Coverage:** Increase the robustness of models to handle more languages effectively.
- **Enhance Content Preservation:** Continue improving methods to ensure that the original meaning of texts is retained post-detoxification.
- **Refine Evaluation Metrics:** Develop more nuanced metrics that can better capture the subtleties of language detoxification.

## Contributions
Contributions to this project are welcome, especially in areas of model tuning, dataset expansion, and translation of detoxification techniques to new languages.

---

## Experiment Results

### Results of CoPA selection from mT5 and delete-baseline candidate predictions on dev-set

| Model    | J-score   |
|----------|-----------|
| XGLM-564M| 0.28452   |
| XGLM-1.7B| 0.28440   |

