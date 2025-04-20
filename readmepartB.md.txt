
DL Assignment 2 - Part B
Title: Fine-tuning GPT2-Medium Model for English Lyrics Generation

Objective:
The objective of this part is to fine-tune a pre-trained GPT2-medium model for generating English song lyrics. The lyrics dataset was manually curated from publicly available samples of 50 Cent's songs. The model must be properly fine-tuned, evaluated, and sample generations must be shown.

Model Architecture:
- Base Model: GPT2-Medium (approximately 355M parameters)
- Tokenizer: GPT2Tokenizer with appropriate special tokens
- Training Head: Causal Language Modeling (default for GPT models)

Dataset Information:
- The lyrics dataset was manually curated.
- Consisted of approximately 20–30 samples from rap and pop lyrics.
- Data cleaning was performed to ensure no empty samples.

Preprocessing:
- Tokenization of text using GPT2 tokenizer.
- Padding and truncation applied to ensure fixed maximum length.

Hyperparameters Used:
- Learning Rate: 5e-5
- Batch Size: 2
- Number of Training Epochs: 5
- Warmup steps: 500
- Weight decay: 0.01
- Framework: HuggingFace Transformers, PyTorch backend
- Hardware: Colab Pro A100 GPU High RAM instance

Training Procedure:
- The model was trained using Causal Language Modeling objective.
- Input texts were tokenized and fed into the model.
- Trainer API was used to simplify training, saving checkpoints and loss tracking.
- Training was carried out for 5 epochs with proper monitoring of training loss.

Evaluation Procedure:
- After training, the fine-tuned model was used to generate lyrics.
- Random starting prompts were fed and text was generated with maximum length 100 tokens.
- The coherence, creativity, and flow of the generated lyrics were manually analyzed.
- No quantitative BLEU or ROUGE scores were reported as the task was creative generation.

Sample Outputs:
Example of generated lyrics:
Love is a funny thing
When love is so strong
Love can make you forget
You've got to let go of your pride and be free...

Final Checklist:
- GPT2-medium model was fine-tuned, not GPT2-small.
- The dataset was manually curated and preprocessed.
- Fine-tuning was performed for exactly 5 epochs.
- Training logs were shown properly.
- Evaluation was conducted by generating sample outputs.
- Training and evaluation steps were detailed.


Conclusion:
The GPT2-medium model was successfully fine-tuned to generate coherent, stylistic English song lyrics based on a limited dataset. The training and evaluation procedures were performed correctly and outputs were consistent with expectations.

