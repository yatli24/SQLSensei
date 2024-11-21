# SQLSensei - Your Go-To SQL assistant

This repo documents the development of a fine-tuned LLM whose purpose is to generate the most accurate SQL queries possible.

SQLSensei can confidently and correctly generate basic to intermediate SQL queries when provided the appropriate context and table information. However, correctly generating advanced queries, such as those found in the Spider 2.0 dataset, remains a challenge for this model.

### Features
- 91% Testing Accuracy (ROGUE Metrics)
- Trained on over 118000 labeled SQL queries using T5

### Datasets
- All available on Hugging Face
  - https://huggingface.co/datasets/knowrohit07/know_sql
  - https://huggingface.co/datasets/b-mc2/sql-create-context
  - https://huggingface.co/datasets/Clinton/Text-to-sql-v1

### Module Dependencies
- PyTorch
- Transformers
- Evaluate
- Datasets (Hugging Face)

### Requirements for Training
- Hugging Face API Token
- wandb API Token

### Implementation
- Python (Jupyter Notebook, Google Colab)
