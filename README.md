# Brain--Tumor--Detector
"This code detects brain tumors in MRI images using a pre-trained model. The user provides the image file path, and the image is processed to fit the model's input format. The model predicts whether a tumor is present, printing "No tumor detected" for 0 or "Tumor detected" for 1. It includes error handling for invalid image paths.

This code is designed to detect brain tumors in MRI images using a pre-trained machine learning model. Here's a detailed description:

Model Loading: The script first loads a pre-trained deep learning model (BrainTumor10epochs.h5) using Keras' load_model function.

User Input for Image Path: The user is prompted to enter the file path of the MRI image they want to test. The image file is then loaded using OpenCV's cv2.imread() function.

Error Handling: If the image file is invalid or not found, an error message is displayed.

Image Preprocessing:
The loaded image is converted into a format that is compatible with the model by first converting it into a PIL image (Image.fromarray).
It is resized to 64x64 pixels (the size expected by the model) and then converted into a NumPy array.

Model Prediction: The processed image is expanded into the required dimensions for model input and passed into the model for prediction. The model outputs a prediction that indicates whether a tumor is present.

Classification:
If the model's prediction result is 0, the script prints "No tumor detected."
If the result is 1, it prints "Tumor detected."
