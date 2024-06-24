# Fine-Tuning-on-ECG-Data

## Purpose and Context

The goal of this project is to predict vascular age using ECG (Electrocardiogram) data along with demographic information of subjects. Three models — Cohere, Llama-2-13b, and Idefics-9b — are utilized to fine-tune and predict vascular age based on the collected data.

## Model: Cohere

### Training Process

- **Data Splitting**: The initial dataset is split using the `train_test_split` function from sklearn. This function divides the data into two parts: 80% for training (`train`) and 20% for testing (`test`).

- **Data Formatting**: The training data is then formatted into a specific text generation format required by the Cohere model. This format includes all relevant ECG features and demographic details, structured as a "user_message".

- **Model Output**: During training, the Cohere model predicts the vascular age based on the input data. The output of this prediction is generated under the section called "chatbot_message".

- **File Output**: The predictions are saved in a `.jsonl` file format. This file contains the predicted vascular age for each subject.

### Prediction Phase

- **Input Data**: For making predictions using the fine-tuned Cohere model, a large CSV file is used. This CSV file contains data for hundreds of subjects, including their ECG features and demographic information.

- **Prediction Output**: The fine-tuned Cohere model applies its predictive capability to this dataset. It generates predictions for the vascular age of each subject in the CSV file.

- **Output Format**: The predictions from the model are stored in a CSV format. This allows for easy analysis and further processing of the predicted vascular ages.

## Model: Llama-2-13b
This project involves a text generation model that has been fine-tuned on ECG (Electrocardiogram) data and deployed privately on Hugging Face's model hub. The model specializes in predicting the vascular age of subjects based on their ECG features and demographic information.

### Deployment Details

- **Platform**: The model is hosted on Hugging Face's model hub, a platform for sharing and deploying machine learning models.
  
- **Adjustable Parameters**: Users can adjust several parameters to tailor the model's behavior:
  - **Qlora**: Configuration or settings related to the model's architecture or fine-tuning process.
  - **SFT**: Special Fine-Tuning parameters, possibly involving customized training procedures.
  - **bitsandbytes**: Technical configurations or optimizations for deployment.
  - **Training Arguments**: Parameters controlling training specifics such as batch size, learning rate, and epochs.

### Fine-Tuning Process

- **Data Splitting**: The initial dataset is split into 20% test and 80% train sets to assess model performance and prevent overfitting.
  
- **Supervised Fine-Tuning**: The model undergoes supervised fine-tuning using a trainer, learning from ECG data and associated vascular age labels.

### Model Usage

- **User Interaction**: Users interact with the model by providing inputs related to ECG features or demographic information of a subject.
  
- **Output**: Based on the user's input, the model generates predictions for the vascular age of the subject. This output estimates the age of blood vessels based on ECG data, crucial for cardiovascular health assessment.


## Model: Idefics-9b

