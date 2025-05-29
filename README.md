# Pneumonia Detection using CNN and GUI

This project implements an automated pneumonia detection system using chest X-rays. A custom Convolutional Neural Network (CNN) model is trained and a PyQt5-based GUI is provided for easy interaction. The user can upload a chest X-ray image, and the system predicts whether the person has pneumonia.

## Features
- **Model**: Uses VGG16-based custom CNN for pneumonia detection.
- **GUI**: PyQt5-based graphical interface for uploading chest X-rays and receiving predictions.
- **Speech Feedback**: The system provides voice-based feedback on the prediction.

## Prerequisites

1. Python 3.6 or higher.
2. Install the required Python libraries using `pip`:

    ```bash
    pip install -r requirements.txt
    ```

### Required Libraries:
- `tensorflow`
- `keras`
- `PyQt5`
- `Pillow` (for image processing)
- `pywin32` (for speech synthesis on Windows)
- `numpy`
- `matplotlib`
- `warnings`

### Additional Notes:
- **Windows users**: Ensure that `pywin32` is installed for the speech synthesis functionality (`win32com.client`).
- **Mac/Linux users**: Replace the speech functionality with a platform-appropriate library (such as `pyttsx3`).

## Dataset
The model is trained on the [Kaggle Chest X-Ray dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia). Ensure that you download the dataset and place it in a folder named `Datasets` with subdirectories `train`, `test`, and `val` as expected by the code.

## File Structure
- chest_xray_detection.py # Model training script using CNN (VGG16).
- pneumonia_detection_gui.py # PyQt5-based GUI for prediction.
- chest_xray.h5 # Trained CNN model file.
- Datasets/ # Contains chest X-ray images (train/test/val folders).
- picture.gif # GIF used in the GUI.
- requirements.txt # List of dependencies.


## How to Run

### Step 1: Train the Model (optional)

If you want to retrain the model, run the `chest_xray_detection.py` script:

```bash

python chest_xray_detection.py

```

This script will train a CNN model using the VGG16 architecture on the chest X-ray dataset and save the trained model as chest_xray.h5.

### Step 2: Run the GUI

Once the model is trained (or if you are using the pre-trained model), run the GUI application:

```bash

python pneumonia_detection_gui.py

```

This will launch a GUI where you can upload a chest X-ray image and get a prediction. The system will output whether the person is affected by pneumonia or is normal, along with a voice output of the result.

## Usage
- Click on the Upload Image button to select a chest X-ray image.
- After selecting the image, click on Prediction.
- The system will show and speak the result (whether the person is affected by pneumonia or normal).


### Notes:
1. Code blocks for commands like `pip install` or `python` are wrapped with triple backticks (```` ```bash ```` for bash commands).
2. Regular text, file structure, and lists follow normal markdown syntax.
3. Images (like `screenshot.png`) should be referenced using `![Image description](image-url.png)`.

Make sure you name the file `README.md` and place it in the root of your project folder for GitHub to render it correctly.
