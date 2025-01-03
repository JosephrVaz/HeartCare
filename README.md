# Heart Failure Prediction and Personalized Treatment Recommendations

## Project Overview

This project develops a hybrid system that combines a finetuned T5 model with a classification model to predict heart failure risk and provide personalized treatment recommendations. 

Cardiovascular diseases, including heart failure, are a leading cause of mortality worldwide. Early and accurate prediction of patient risk, coupled with personalized treatment recommendations, is crucial for improving outcomes and reducing healthcare burdens. However, traditional risk assessment methods often lack precision, and generalized treatment guidelines may not be optimal for individual patients with unique characteristics.

## Project Aim

To develop a hybrid system that accurately predicts the risk of heart failure in individual patients and provides personalized treatment recommendations, ultimately aiming to improve patient outcomes and reduce healthcare burdens associated with heart failure management.

## Methodology

### 1. Finetuning T5

- A pre-trained T5 model ("google/flan-t5-small") is finetuned on a dataset of patient characteristics and corresponding treatment recommendations.
- The dataset is preprocessed, tokenized, and converted into a suitable format for training the T5 model.
- The T5 model learns to generate personalized treatment recommendations based on patient-specific input.

### 2. Classification Model

- A logistic regression model is trained to predict the risk of heart failure (death event).
- The model uses relevant clinical features (e.g., age, anemia, creatinine levels) as input.
- Hyperparameter tuning is performed using GridSearchCV to optimize the model's accuracy.

### 3. Inference

- The classification model predicts the risk of heart failure for a new patient.
- The patient's clinical data and the risk prediction are combined to form a prompt for the finetuned T5 model.
- The T5 model generates personalized treatment recommendations based on the prompt.

### 4. Evaluation

- The quality of the generated recommendations is evaluated using the BLEU score.
- The BLEU score measures the similarity between the generated recommendations and a reference set of recommendations.
- Higher BLEU scores indicate better alignment with expected recommendations.

## Results

- The finetuned T5 model demonstrates the ability to generate personalized treatment recommendations based on patient characteristics and predicted risk.
- The classification model achieves a reasonable accuracy in predicting heart failure risk.
- The BLEU score provides a quantitative measure of the quality and relevance of the generated recommendations.

## Future Work

- Explore other advanced language models for recommendation generation.
- Incorporate more comprehensive patient data, including medical history and imaging data.
- Develop a user interface for easier interaction with the system.
- Validate the system's performance on a larger and more diverse patient population.

## Usage

1. **Install required libraries:**
## License
This project is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License. See the [LICENSE](./LICENSE) file for details.
