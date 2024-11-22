# SQLSensei - Your Go-To SQL assistant

This repo documents the development of a fine-tuned LLM whose purpose is to generate the most accurate SQL queries possible, referencing an existing study available for viewing here: https://huggingface.co/cssupport/t5-small-awesome-text-to-sql

SQLSensei can confidently and correctly generate basic to intermediate SQL queries when provided with the appropriate context and table information. However, correctly generating advanced queries, such as those found in the Spider 2.0 dataset, remains a challenge for the model. SQLSensei was developed using an NVIDIA GTX 1060 GPU, which unfortunately limited the efficiency of training with larger datasets, more epochs, and higher performance hyperparameters.

### Repo Contents
- SQLSensei.inbpy - Source code for SQLSensei

### Features
- 90% Testing Accuracy (ROGUE Metrics)
- Trained on over 118000 labeled SQL examples

### Datasets
- All available on Hugging Face
  - https://huggingface.co/datasets/knowrohit07/know_sql
  - https://huggingface.co/datasets/b-mc2/sql-create-context
  - https://huggingface.co/datasets/Clinton/Text-to-sql-v1

### Dependencies
- PyTorch
- Transformers
- Evaluate
- Datasets (Hugging Face)

### Requirements for Training
- Hugging Face API Token
- wandb API Token
- ~4 hours training time (NVIDIA GeForce GTX 1060)

### Implementation
- Python (Jupyter Notebook, Google Colab compatible)
