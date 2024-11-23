# Introduction
Transformer-based models have proven to be powerful tools in machine learning. Fine-tuning these models enables them to adapt to custom datasets and improve performance for specific tasks. This project focuses on the fine-tuning of an existing model, provided by a previous study to generate accurate SQL queries, with a focus on computational resource convenience and performance optimization.

# Task
Using the Hugging Face API, a small pre-trained T5 model and tokenizer were fine-tuned on a dataset of natural language-to-SQL pairs. The goal was to minimize the model's loss on validation and test datasets.

# Data Preprocessing
Some preprocessing was conducted to ensure compatibility with the T5 architecture. The dataset was cleaned, split, formatted, and then tokenized. While cleaning, shuffling was done to ensure variability of the training data. 

# Limitations
The fine-tuning process encountered several challenges, primarily due to the computational limitations of the Nvidia GeForce GTX 1060 GPU with 6GB of VRAM. This restricted the selection of hyperparameters such as batch size and epochs. Additionally, generating accurate SQL queries using more complex and larger datasets, such Spider 2.0, posed significant difficulties. Additionally, the source code was dependent on several APIs and modules, namely the Hugging Face API and PyTorch.

# Methods
The Hugging Face Trainer API was extensively utilized for model training and evaluation, and hyperparameters were tuned with respect to the constraints of the GPU, through experimentation. The final set of hyperparameters that were most effective for the Nvidia GTX 1060 GPU included a learning rate of 5e-3, warmup steps of 100, 2 training epochs, and a per-device batch size of 16 for both training and evaluation. Weight decay was set to 0.01, and logging was for every 35 steps, with evaluation calculated at the end of each epoch. Evaluation calculations included test accuracy using the ROGUE metric, and manual inspection to compare generated queries.

# Results
The final model achieved a test accuracy of 90%. Its performance on basic to intermediate queries improved significantly when compared to the base model. However, the computational constraints of the Nvidia GTX 1060 limited the depth of experimentation. As a result, larger and more complex datasets could not be utilized due to hardware restrictions, leaving some avenues for improvement unexplored.

# Performance Insights
Access to more powerful computing resources could unlock many benefits, and the following could be experimented with to improve performance.
- Larger Datasets: Training and testing with more complex datasets would greatly improve utility and generalization.
- Increased Training Epochs: Extended training durations could help the model converge to higher performance levels.
- Hyperparameter Optimization: Larger batch sizes and learning rates could be implemented.

# Conclusion
The development of SQLSensei demonstrates the capabilities of even a small transformer model for SQL query generation, achieving extremely high accuracy despite computational limitations. The results show that larger models may not necessarily be required for accurate SQL generation, and that smaller models may be a more viable and efficient alternative for this task. Future implementations with more computational power and more complex datasets could be explored to further utilize the potential of this model.
