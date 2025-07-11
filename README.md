# Prediksi_Siapa_yang_Introvert_dan_Siapa_yang-_kstrovert

Personality Prediction Project

This project aims to predict whether an individual has an Extrovert or Introvert personality based on behavioral features using a RandomForestClassifier model. The project is implemented in a Jupyter Notebook (Prediksi_Siapa_yang_Introvert_dan_Siapa_yang_Ekstrovert.ipynb).

Project Overview

The notebook processes two datasets:





Training Data: Contains features and labeled personality types (Extrovert or Introvert).



Test Data: Contains features for which predictions are made.

The model uses features such as time spent alone, stage fear, social event attendance, frequency of going outside, feeling drained after socializing, size of friend circle, and social media post frequency to predict personality types.

Dataset





Training Data: Loaded from a Google Drive CSV file with features and the target variable Kepribadian (Personality).



Test Data: Loaded from a Google Drive CSV file without the target variable, used for predictions.



Features:





Waktu_Dihabiskan_Sendirian (Time spent alone)



Rasa_Takut_Tampil_Yes (Stage fear, boolean)



Kehadiran_Acara_Sosial (Social event attendance)



Frekuensi_Keluar_Rumah (Frequency of going outside)



Lelah_Setelah_Bersosialisasi_Yes (Drained after socializing, boolean)



Ukuran_Lingkaran_Pertemanan (Size of friend circle)



Frekuensi_Membuat_Potingan (Post frequency)

Dependencies

The project requires the following Python libraries:





pandas



numpy



matplotlib



seaborn



scikit-learn

You can install them using:
pip install pandas numpy matplotlib seaborn scikit-learn

Usage





Data Loading:





The training and test datasets are loaded from Google Drive using export links generated from file IDs.



Ensure you have access to the datasets or replace the file IDs with your own.



Data Preprocessing:





The test dataset columns are renamed to match the training dataset.



Boolean columns (Rasa_Takut_Tampil_Yes, Lelah_Setelah_Bersosialisasi_Yes) are converted from string ('Yes'/'No') to boolean (True/False).



Missing values are handled implicitly by the RandomForestClassifier.



Model Training:





A RandomForestClassifier is used with random_state=42 and class_weight='balanced' to handle potential class imbalances.



The target variable (Kepribadian) is encoded using LabelEncoder to convert Extrovert and Introvert to numerical values.



Prediction:





Predictions are made on the test dataset.



The encoded predictions are transformed back to Extrovert or Introvert using the inverse transform of LabelEncoder.



Output:





The predictions are saved to a CSV file named submission.csv with columns id and Personality.

Running the Notebook





Ensure you have Jupyter Notebook or JupyterLab installed.



Open the notebook Prediksi_Siapa_yang_Introvert_dan_Siapa_yang_Ekstrovert.ipynb.



Run the cells sequentially to load data, preprocess, train the model, and generate predictions.



The output CSV file (submission.csv) will be saved to the specified path (default: /content/drive/Othercomputers/My Laptop/D:/submission.csv).

Notes





The Google Drive file IDs used in the notebook (data_latih_file_id and data_uji_file_id) must be accessible. If you are using your own datasets, update the file IDs accordingly.



The output CSV file contains the predicted personality labels (Extrovert or Introvert) for each id in the test dataset.



The model assumes the test dataset has the same feature structure as the training dataset after renaming columns.

Output

The final output is a CSV file (submission.csv) with the following structure:





id: Unique identifier for each test sample.



Personality: Predicted personality label (Extrovert or Introvert).

Example:

id,Personality
18524,Extrovert
18525,Introvert
18526,Extrovert
...
