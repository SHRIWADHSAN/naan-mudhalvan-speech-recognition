# naan-mudhalvan-speech-recognition
1)speechtotextpipeline.py
# Speech-to-Text Transcription GUI

This project is a desktop application built with Python and Tkinter that allows users to transcribe audio files (`.wav` and `.mp3`) into text using Google Speech Recognition. It also calculates error metrics such as **Word Error Rate (WER)** and **Character Error Rate (CER)**, and displays a visual chart of the metrics.

## Features

- Transcribe `.wav` and `.mp3` audio files to text
- Automatically convert `.mp3` files to `.wav` format
- Display transcription results in a user-friendly interface
- Calculate and display WER and CER
- Visualize error metrics with a bar char
- Error handling and user notifications via Tkinter

## Dependencies

Make sure the following packages are installed:

```bash
pip install SpeechRecognition pydub numpy jiwer matplotlib
```

You also need to have **ffmpeg** installed for `pydub` to process `.mp3` files.

## How to Run

1. Save the script as `Speechtotextpipeline.py`.
2. Run the script using Python 3:

```bash
python Speechtotextpipeline.py
```

3. Use the GUI to select an audio file and click "Transcribe" to see results.

## File Structure

- `transcribe_audio`: Handles audio conversion and transcription
- `calculate_wer_cer`: Calculates WER and CER using `jiwer`
- `browse_file`, `transcribe_file`: GUI handlers
- `show_metrics_chart`: Displays error metrics visually
- Tkinter-based GUI code at the bottom of the script

## Notes

- Uses Google's online API, so internet connection is required
- Random WER/CER values are used if reference text is not provided

## License

This project is for educational and personal use only.


2)Emotionrecognition.py
# Emotion Recognition from Audio using MFCC Features

This project performs emotion classification from audio features extracted using MFCCs. The model uses the RAVDESS dataset (features saved in `ravdess_mfcc_features.pkl`) and classifies speech into various emotions using machine learning techniques.

## Features
- Uses MFCC (Mel Frequency Cepstral Coefficients) features.
- Classifies emotions using Logistic Regression or Random Forest.
- Includes evaluation via confusion matrix and classification report.

## Requirements
- Python 3.x
- pandas
- numpy
- scikit-learn
- seaborn
- matplotlib

Install dependencies using:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib
```

## Files
- `Emotionrecognition.py`: Main script to run the model.
- `ravdess_mfcc_features.pkl`: Pickled DataFrame with `mfcc` and `emotion` columns.

## How to Run

```bash
python Emotionrecognition.py
```

This will:
- Load MFCC features
- Train a Random Forest classifier (or Logistic Regression)
- Predict emotions
- Display evaluation metrics
- Visualize results via a confusion matrix

## Output
- Predicted emotion labels for each sample
- Accuracy score
- Classification report
- Confusion matrix plot


3)Accentawaresystem.py
# Accent-Aware Speech Recognition System

This Streamlit-based web app predicts the accent of a speaker based on audio file input or manually entered feature vectors. The model uses MFCCs and other spectral features for classification.

## Features
- Web UI for audio upload and prediction
- Real-time accent prediction
- Visual confidence distribution
- Optional custom input testing

## Requirements
- Python 3.x
- streamlit
- numpy
- pandas
- librosa
- soundfile
- joblib
- matplotlib

Install all dependencies using:

```bash
pip install streamlit numpy pandas librosa soundfile joblib matplotlib
```

## Files
- `Accentawaresystem.py`: Main Streamlit app script.
- `accent_model.pkl`: Pretrained classifier.
- `label_encoder.pkl`: Label encoder for accent labels.

## How to Run

```bash
streamlit run Accentawaresystem.py
```

This will:
- Start the web application
- Let you upload `.wav`, `.mp3`, or `.flac` audio
- Show predicted accent and prediction probabilities

## Output
- Accent label (e.g., US, British, Indian, etc.)
- Confidence plot showing probabilities for all classes

