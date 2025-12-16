# Dataset Overview 

The datasets in this repository are primarily designed for the models evaluated in the paper Positional Biases Shift as Inputs Approach Context Window Limits (arXiv:2508.07479).

These datasets are tailored to the specific tokenizers and context window sizes of the evaluated models. When applying the datasets to other models, samples should be regenerated using the target model’s tokenizer, as token counts can vary substantially across tokenization schemes. Because our analysis focuses on relative input length—defined as the number of input tokens relative to a model’s context window size—consistent tokenization is essential for valid comparisons.


## Tokenization Details

Each dataset entry includes the fields model and tokenizer, indicating the models to which the sample applies and the tokenizer used to compute token counts. For LLaMA and Gemma models, we use the GPT-4 tokenizer, following Levy et al. (2024) (arXiv:2402.14848). This choice results in token counts within approximately ±70 tokens of the models’ native tokenizers. For Qwen and Mistral models, we use their native tokenizers, as GPT-4 tokenization introduces significantly larger discrepancies for these architectures.


## Using the Dataset with Other Models

When using this dataset to evaluate additional models, ensure that both the context window size and tokenizer token counts are comparable. If they are not, the base_instances.jsonl file should be used to regenerate samples by padding inputs to the required lengths.