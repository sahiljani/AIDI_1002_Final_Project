# TinyLLM 

This repository contains the code and instructions for fine-tuning the TinyLLM model on a color dataset and using it to describe colors based on their names.

## Folder Structure

- `tinyLLM_model/`: Contains TinyLLM model.
- `contribution/`: TinyLLM with new datasets for evaluation in various contexts.


### Installation

```bash
!pip install accelerate peft bitsandbytes transformers trl

```


## Data Preparation

The color dataset used for fine-tuning is located at `burkelibbey/colors`. The data is reformatted to fit the ChatML format.

## Fine-Tuning

- Load the dataset and prepare the training data.
- Initialize the TinyLLM model and tokenizer.
- Configure LoRA (LoraConfig) and training arguments.
- Train the model using SFTTrainer from trl.

## Merging with Base Model

After fine-tuning, the LoRA is merged with the base TinyLLM model to produce the final model.

## Inference

Generate color descriptions using the fine-tuned TinyLLM model.

## Usage

1. Fine-tune the TinyLLM model by running the provided notebook.
2. dd the Hugging Face token to your notebook with the name HF_TOKEN as the Secret key.
3. Generate color descriptions using the `generate_response` function.

```python
generate_response(user_input='Yellow color')
```

