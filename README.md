# nmt_thesis

# IndicTrans2 English-to-Indic Translation Pipeline

This repository contains a Jupyter notebook for training and evaluating a Seq2Seq translation model using [ai4bharat/indictrans2-en-indic-dist-200M](https://huggingface.co/ai4bharat/indictrans2-en-indic-dist-200M) for English-to-Indic language translation.

## Features

- Loads and preprocesses English-to-Indic datasets (BPCC, FLORES-200).
- Trains a transformer-based translation model with early stopping and WandB logging.
- Evaluates model performance using BLEU, METEOR, and CHRF++ metrics.
- Supports flexible language selection via ISO 639-3 codes.

## Setup

1. Clone the repository.
2. Install dependencies:
    ```sh
    pip install datasets IndicTransToolkit evaluate transformers wandb tqdm
    ```
3. Set up your HuggingFace and WandB API tokens (see notebook for details).

## Usage

Open [`nmt_it2_raghav_qm.ipynb`](c:\Users\sanje\Downloads\nmt_it2_raghav_qm.ipynb) in Jupyter or VS Code and run the cells sequentially to:

- Install dependencies
- Authenticate with HuggingFace and WandB
- Load and preprocess data
- Train the model
- Evaluate translation quality

## Customization

- Change `selected_language` in the configuration cell to train for a different Indic language.
- Adjust training parameters in the `Seq2SeqTrainingArguments` section as needed.

## Evaluation

The notebook includes robust evaluation functions that automatically select FLORES-200 or BPCC datasets and compute translation metrics.


## Acknowledgements

- [AI4Bharat](https://ai4bharat.org/)
- [HuggingFace](https://huggingface.co/)
- [WandB](https://wandb.ai/)
- A huge thank you to my supervisor, Prof. Arkaitz Zubiaga and Queen Mary, University of London for their support and guidance throughout this masters thesis. 
