# Handwritten-Text-Recognition-with-Streamlit-and-TrOCR
This project demonstrates a simple web application built using Streamlit, integrated with Hugging Face Transformers for handwritten text recognition using a pre-trained model from the TrOCR family by Microsoft.
The app allows users to upload an image, extract handwritten text using OCR (Optical Character Recognition), and display the extracted text.

## Features
Upload and View Image: Users can upload .jpg images of handwritten text.
Handwritten Text Recognition: The app uses a pre-trained Transformer-based OCR model to extract text from the uploaded image.
User-Friendly Interface: Built with Streamlit, the app provides a simple, intuitive interface.
Real-time Extraction: Displays the extracted text after processing the image.
Setup and Installation

## Prerequisites
Python 3.7+
Ngrok (for exposing the local app to the web)

## Dependencies
Streamlit: Used for building the web interface.
Pyngrok: For exposing the app to the web.
Transformers: Provides pre-trained models for OCR (Optical Character Recognition).

## Application Overview
app.py
The main Streamlit app (app.py) does the following:

Imports Libraries:

Loads the necessary Python libraries such as streamlit, transformers, PIL (Pillow), and torch.
Model Setup:

Initializes the TrOCRProcessor and VisionEncoderDecoderModel for OCR.
OCR Functionality:

Processes the uploaded image and uses the model to predict the text.
Streamlit Interface:

Displays a title, prompts the user to upload an image, and shows the extracted text.
Ngrok Integration:

Uses pyngrok to expose the Streamlit app to the web.

## Example Workflow
User uploads a handwritten image.
The app processes the image using the pre-trained model.
The extracted text is displayed on the app interface.

## Code Breakdown

![image](https://github.com/user-attachments/assets/8903a554-9224-4432-af43-b55ba31f3d12)

This function starts the Streamlit app in a separate thread, ensuring it runs headlessly on port 8501.

![image](https://github.com/user-attachments/assets/00b7875b-4c40-4153-96e0-14065e547f23)

This function handles the OCR process by transforming the input image and decoding the output into text.

![image](https://github.com/user-attachments/assets/34fafae0-9890-40bb-9c76-2e3a92e8d62a)

The Ngrok token is used to expose the local Streamlit app to the web, making it accessible via the generated public URL.

## Running the Application
Once the app is running, users can access it by navigating to the provided Ngrok URL. The app interface allows uploading an image, and it will display the extracted handwritten text.

## Example Output

After uploading a handwritten image, the application will display the recognized text below the image.
![image](https://github.com/user-attachments/assets/4e7512d4-b291-43c2-89db-9833de7a69b9)

## Future Improvements

Multiple Image Formats: Add support for additional image formats such as PNG, GIF, and BMP.
Enhanced Text Extraction: Improve the accuracy by fine-tuning the model on more datasets.
Multi-language Support: Extend the functionality to recognize handwritten text in different languages.
Styling and Design: Improve the UI to make it more appealing and responsive.

