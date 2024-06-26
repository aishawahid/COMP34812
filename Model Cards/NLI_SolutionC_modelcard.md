---
{}
---
language: en
license: cc-by-4.0
tags:
- pairwise-text-classification
repo: https://github.com/aishawahid/COMP34812

---

# Model Card for x48913aw-t09329lw-NLI

<!-- Provide a quick summary of what the model is/does. -->

This is a classification model that was trained to
      detect whether a premise confirms a hypothesis.


## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->

This model is an ensemble model combining roBERTa, T5 and FlanT5. With an additonal BiLSTM layer used in the classification head.

- **Developed by:** Aisha Wahid and Libby Walton
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** Transformers
- **Finetuned from model [optional]:** 
    - roberta-base
    - t5-base
    - flan-t5-base

### Model Resources

<!-- Provide links where applicable. -->

- **Repository:** 
    - https://huggingface.co/FacebookAI/roberta-base
    - https://huggingface.co/google-t5/t5-base
    - https://huggingface.co/google/flan-t5-base
- **Paper or documentation:** NA

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

All 26k training pairs were used.

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->


      - learning_rate: 1e-5
      - optimiser: sgd
      - train_batch_size: 32
      - eval_batch_size: 32
      - num_epochs: 8-10
      - dropout: 0.3
      - activation: sigmoid

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->


      - overall training time: 3 hours
      - duration per training epoch: 350 seconds
      - model size: 2.64GB

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

### Testing Data & Metrics

#### Testing Data

<!-- This should describe any evaluation data used (e.g., the development/validation set provided). -->

All 6k validation pairs were used.

#### Metrics

<!-- These are the evaluation metrics being used. -->


      - Accuracy
      - Precision Macro
      - Recall Macro
      - F1-score Macro
      - Precision Weighted Macro
      - Recall Weighted Macro
      - F1-score Weighted Macro

### Results

The model obtained an Accuracy of 89.3%, a Precision Macro of 89.3%, a Recall Macro of 89.3%, an F1-score Macro of 89.3%, a Precision Weighted Macro of 89.3%, a Recall Weighted Macro of 89.3%, F1-score Weighted Macro of 89.3%.

## Technical Specifications

### Hardware


      - RAM: at least 16 GB
      - Storage: at least 3GB,
      - GPU: L4

### Software


      - Transformers 4.38.2
      - Tensorflow 2.15.0

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

Any inputs (concatenation of two sequences) longer than
      120 tokens will be truncated by the model.

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The hyperparameters were determined by experimentation
      with different values.
