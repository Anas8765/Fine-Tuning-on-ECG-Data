# Fine-Tuning-on-ECG-Data

**Purpose and Context**

The goal is to predict vascular age using ECG (Electrocardiogram) data along with demographic information of subjects. Three models — Cohere, Llama-2-13b, and Idefics-9b — are employed to fine-tune and predict this vascular age based on the collected data.

**Model: Cohere**
***Training Process:***

- ****Data Splitting****: The initial dataset is split using the train_test_split function from sklearn. This function divides the data into two parts: 80% for training (train) and 20% for testing (test).

- Data Formatting: The training data is then formatted into a specific text generation format required by the Cohere model. This format includes all relevant ECG features and demographic details. These are structured as a "user_message".

- Model Output: During training, the Cohere model predicts the vascular age based on the input data. The output of this prediction is generated under the section called "chatbot_message."

- File Output: The predictions are saved in a .jsonl file format. This file contains the predicted vascular age for each subject.

***Prediction Phase:***

    Input Data: For making predictions using the fine-tuned Cohere model, a large CSV file is used. This CSV file contains data for hundreds of subjects, including their ECG features and demographic information.

    Prediction Output: The fine-tuned Cohere model applies its predictive capability to this dataset. It generates predictions for the vascular age of each subject in the CSV file.

    Output Format: The predictions from the model are stored in a CSV format. This allows for easy analysis and further processing of the predicted vascular ages.
