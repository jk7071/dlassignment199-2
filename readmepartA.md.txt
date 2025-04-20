
DL Assignment 2 - Part A
Title: Transliteration Using Encoder-Decoder (LSTM-based Seq2Seq Model)

Objective:
The objective of this part is to implement a character-level Encoder-Decoder (Sequence-to-Sequence) model using LSTM cells. The goal is to transliterate Latin-script (English) words into Devanagari-script (Hindi) words. The model must be flexible enough to modify embedding size, hidden state size, number of layers, and the type of recurrent cell.

Model Architecture:
- Encoder: LSTM layer
- Decoder: LSTM layer followed by Dense layer with softmax activation
- Input embedding layer for encoder inputs
- Flexibility to change embedding dimension, hidden state size, and number of LSTM layers

Dataset Information:
- Dataset manually curated from the Hindi subset of the Dakshina dataset.
- Only Hindi transliteration files were used.
- Preprocessing was done to prepare parallel input-output character sequences.

Hyperparameters Used:
- Embedding size: 256
- Hidden state size: 256
- Number of LSTM layers: 1
- Batch size: 64
- Optimizer: Adam
- Loss function: Sparse categorical crossentropy
- Number of epochs: 30

Training Procedure:
- The dataset was split into training, validation, and test sets.
- Latin-script input sequences were one-hot encoded.
- Devanagari-script target sequences were one-hot encoded.
- Training was done using teacher forcing where the decoder receives the ground truth token at each timestep.

Evaluation Procedure:
- After training, predictions were generated character-by-character.
- Accuracy was computed by comparing the predicted sequence with ground truth.
- Evaluation was performed on a held-out test set.

Final Computation and Parameters Derived:
- Computations: T × [4(m+k)k + 8k² + kV]
- Parameters: 4(m+k+1)k + 4(2k+1)k + (kV+V)

Sample Outputs:
Examples from test data:
- Input: 'ankit' → Actual: 'अंकित' → Predicted: 'अंकित'
- Input: 'delhi' → Actual: 'दिल्ली' → Predicted: 'दिल्ली'

Final Checklist:
- Flexibility in embedding size, hidden size, number of layers is implemented.
- Encoder and decoder implemented using LSTM cells.
- Training conducted properly for 30 epochs.
- Evaluation performed and accuracy reported.
- Computation and parameter formulas were derived correctly.
- Sample outputs were collected and displayed.

Conclusion:
The transliteration system was successfully developed and evaluated. The model achieved reasonable performance on unseen Hindi transliterations with a simple LSTM encoder-decoder design.

